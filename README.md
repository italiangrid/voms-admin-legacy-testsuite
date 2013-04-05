# VOMS Admin Web Service test suite

This repository hosts the CERN VOMS Admin legacy test suite.

## Usage

### Prerequisites for the testsuite execution

1. A freshly configured VO supporting the IGI test CA, with the VO_Admin igi test ca certificates
configured with VO admin rights.
2. A valid VOMS proxy obtained from the VO_Admin certificate.
3. VOMS admin client installed on the machine running the tests

### Configure the testsuite

Edit the config file and set

```bash
# The location of the IGI test ca certificates
CERT_DIR="/usr/share/igi-test-ca" 

# The name of the VO under test
vo_name="vo.7" 
```

Then run the testsuite as follows:
```bash
./myCheck-VOMS -n $HOST -l test-sequence.lst.voms-admin
```

where `$HOST` is the host where VOMS Admin is running.
