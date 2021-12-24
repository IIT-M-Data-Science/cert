# cert
CLI certificate PDF generation script. Made for IITM-POD

*Note* The CLI doesn't support QR generation/verification, you must implement your own logic to fit your needs.
# Templates

Add your custom templates under `template` folder.

### `basic` Template

The `basic` template, used by IITM-POD, contains the generic design for the certificate. 

It supports two variants for no of signatures:
- One: The signature will be centered, and the QR will be below the signature.
- Two: The signature will on the either side, and the QR will be centered.
# Example Usage

Setup a virtualenv, and install the dependencies

```bash
pip install -r requirements.txt
```

You can then generate the PDF using command line arguments, for example

```bash
python generate.py -n ALLO -s "President,Student Council,~/IITM/t/s1.png" "Secretary,SARANDA,~/IITM/t/s2.png" -ct basic -e "TestEvent, DotePOD, 09-10-2030"
```

Use `python generate.py -h` to get more info on these arguments.
