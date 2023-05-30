# BitOffinder
Algorithms for CRISPR off-target search in the genome 


//
//       ____   _  _     ___    __   __  _             _
//      | __ ) (_)| |_  / _ \  / _| / _|(_) _ __    __| |  ___  _ __
//      |  _ \ | || __|| | | || |_ | |_ | || '_ \  / _` | / _ \| '__|
//      | |_) || || |_ | |_| ||  _||  _|| || | | || (_| ||  __/| |
//      |____/ |_| \__| \___/ |_|  |_|  |_||_| |_| \__,_| \___||_|
//

Version 5.1

Created by AMICHAI MALLE & ELIAV COHEN

NAME
	Off Target Finder - A tool to find off-target sites for CRISPR/Cas9

USAGE
    <command> [-m <int> -b <int>] [-d <int>] [-pam <string>] [-pam_m <int>]
 	      [-output <file_path>] [-guide <file_path>] [-chr <file_path>] [-chr_max <int>] [-h help]

DESCRIPTION
    -m  <max_mismatch>      The maximum number of mismatches allowed in the off-target sites

    -b <max_bulge>          The maximum number of bulges allowed in the off-target sites

    -d <max_distance>	    The maximum total distance allowed - a total threshold, when set 
			    max_bulge and max_mismatch will be equal to max_distance

    -output <output_file>   [default = './output.txt'] The output path and file name of the off-target sites
                            output list

    -guide <guide_file>     [default = './guides.txt'] The path and file name of the guide file
                            the file should contain one guide sequence per line

    -chr <chr_file>         [default = './chr1.txt'] The path and file name of the 1st chromosome file
                            first chromosome file should be named 'chr1.txt' and the rest of the
                            files should be named 'chr2.txt', 'chr3.txt', etc.

    -pam <pam>		    [default = no pam] A pam string to search as suffix of the target
			    support all variant (example: NGG)

    -pam_m <max_pam_mismatch> 		[default = 0] allow max mismatch for pam searching
					notice that N char will be always match.

    -chr_max <max_chromosome_length>    [default = 300000000] The maximum length of the chromosome files
                                        the program will allocate memory for the chromosome files according
                                        to this value
