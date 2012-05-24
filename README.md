# OVERVIEW

Elesai is a wrapper around LSI's Megacli utility that provides access to the most common types of information required from said utility without the need to speak martian. It is a line-oriented tool so that it can be combined with other Unix command-line tools to process and manipulate the data. It also provides a Nagios check action (in both active and passive modes) which monitors the health of the array and its components and reports 
it accordingly.

# SYNOPSIS

    elesai [global-options] <action> [action-options] <component>

where:

* **`action`** is one of **`show`** or **`check`**
* **`component`** is one of `adapter`, `virtualdrive` (or `vd`) or `physicaldrive` (or `pd`) for **`show`** and `active` or `passive` for **`check`**

Global options include:

* a `--noop` (or `-n`) mode
* a `--debug` (or `-d`) mode

# Sample Output

    gerir@boxie:~: elesai show pd | sort -k 4
    [PD]   e253s3   27       online:spunup     1.82TB   HDD  SATA   0   0   9WM1B7VDST32000644NS SN11
    [PD]   e252s7   23       online:spunup     1.82TB   HDD  SATA   0   0   9WM1FX1LST32000644NS SN11
    [PD]   e253s0   24       online:spunup     1.82TB   HDD  SATA   0   0   9WM1GF2NST32000644NS SN11
    [PD]   e253s1   25       online:spunup     1.82TB   HDD  SATA   0   0   9WM1GY85ST32000644NS SN11
    [PD]   e252s6   22       online:spunup     1.82TB   HDD  SATA   0   0   9WM1GYKJST32000644NS SN11
    [PD]   e253s2   26       online:spunup     1.82TB   HDD  SATA   0   0   9WM1HA0NST32000644NS SN11
    [PD]   e253s5   29       online:spunup     1.82TB   HDD  SATA   0   0   9WM7L834ST32000644NS SN12
    [PD]   e252s4   12       online:spunup   223.06GB   SSD  SATA   0   0   CVPR138405AQ300EGN INTEL SSDSA2CW300G3 4PC10362
    [PD]   e252s2    9       online:spunup   223.06GB   SSD  SATA   0   0   CVPR140100MQ300EGN INTEL SSDSA2CW300G3 4PC10362
    [PD]   e252s0   11       online:spunup   223.06GB   SSD  SATA   0   0   CVPR140201KZ300EGN INTEL SSDSA2CW300G3 4PC10362
    [PD]   e252s1   10       online:spunup   223.06GB   SSD  SATA   0   0   CVPR141300K9300EGN INTEL SSDSA2CW300G3 4PC10362
    [PD]   e252s3    8       online:spunup   223.06GB   SSD  SATA   0   0   CVPR141301KG300EGN INTEL SSDSA2CW300G3 4PC10362
    [PD]   e253s4   30     degraded:spunup     1.82TB   HDD  SATA   0   0   9WM5Y4AEST32000644NS SN12
    [PD]   e252s5   13     hotspare:spunup   223.06GB   SSD  SATA   0   0   CVPR140100TT300EGN INTEL SSDSA2CW300G3 4PC10362
    
# STATUS

Very much in progress. The tool does not yet poke MegaCli itself.



