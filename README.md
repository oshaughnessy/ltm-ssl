# ltm-ssl

Manage SSL certificates and profiles on F5 Local Traffic Managers

This script uses the F5 iControl RESET interface. See also:
https://devcentral.f5.com/wiki/iControlrest.HomePage.ashx


## Requirements

Define the location and credentials for connecting to your F5 LTM. In the script,
change these:

    LTM_HOST = 'FIXME'
    LTM_USER = 'FIXME'
    LTM_PASS = 'FIXME'

or pass them using command-line options:

  --ltm-host LTM_HOST   Hostname or IP address of the F5 LTM (default: FIXME)
  --ltm-user LTM_USER   Username for REST API authentication to the LTM
                        (default: FIXME)
  --ltm-password LTM_PASSWORD
                        Password for REST API authentication to the LTM
                        (default: i've got a secret!)


## Usage

From `ltm-ssl -h`:

    usage: ltm-ssl [-h] [--cert CERT] [--chain CHAIN] [--key KEY] [--status]
                   [--profile PROFILE] [--server SERVER] [--show-profile]
                   [--show-servers] [--show-cert] [--show-key]
                   [--create | --delete | --replace] [--associate | --dissociate]
                   [--version] [-v] [--context {clientside,serverside,all}]
                   [--ltm-host LTM_HOST] [--ltm-user LTM_USER]
                   [--ltm-password LTM_PASSWORD]

    Manage SSL certificates and profiles on an F5 Local Traffic Manager

    optional arguments:
      -h, --help            show this help message and exit
      --cert CERT           Signed public certificate in PEM format
      --chain CHAIN         Certificate chain for the signed certificate
      --key KEY             Private key in PEM format
      --status              Print the state of the profile
      --profile PROFILE     Name of the SSL profile to work with
      --server SERVER       Work with the given virtual server; can be used
                            multiple times
      --show-profile        Show verbose information about the profile
      --show-servers        Show verbose information about the server profiles
      --show-cert           Show verbose information about the SSL certificate
      --show-key            Show verbose information about the SSL key
      --create              Create a new SSL profile
      --delete              ... or delete one
      --replace             ... or replace one (mutually exclusive)
      --associate           Assign the profile to the given server(s)
      --dissociate          Remove the profile from the given server(s)
      --version             print the version number (0.1)
      -v, --verbose         increase output verbosity
      --context {clientside,serverside,all}
                            Apply changes to the client or server side of the
                            virtual server
      --ltm-host LTM_HOST   Hostname or IP address of the F5 LTM (default: FIXME)
      --ltm-user LTM_USER   Username for REST API authentication to the LTM
                            (default: FIXME)
      --ltm-password LTM_PASSWORD
                            Password for REST API authentication to the LTM
                            (default: i've got a secret!)
