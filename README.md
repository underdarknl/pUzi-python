# pUZI python
Proficient UZI pass reader in python, based on work by anne-jan: https://github.com/anne-jan/pUZI-php

## Requirements

* python >= 3.6

Apache config (or NginX equivalent):
```apacheconf
SSLEngine on
SSLProtocol -all +TLSv1.3
SSLHonorCipherOrder on
SSLCipherSuite ECDHE-RSA-AES128-GCM-SHA256:ECDHE-RSA-AES256-GCM-SHA384:ECDHE-RSA-CHACHA20-POLY1305:DHE-RSA-AES128-GCM-SHA256:DHE-RSA-AES256-GCM-SHA384
SSLVerifyClient require
SSLVerifyDepth 3
SSLCACertificateFile /path/to/uziCA.crt
SSLOptions +StdEnvVars +ExportCertData
```

## Usage

```python
import uzireader
uzipas = uzireader.UziPassUser(env[], env[cert])
print(uzipas)
```

```text
{'givenName': 'john', 'surName': 'doe-11111111', 'OidCa': '2.16.528.1.1003.1.3.5.5.2', 'UziVersion': '1', 'UziNumber': '11111111', 'CardType': 'N', 'SubscriberNumber': '90000111', 'Role': '01.015', 'AgbCode': '00000000'}
```

## Uses

[Python cryptography Library](https://cryptography.io/en/)

## Contributing

1. Fork the Project

2. Ensure you have Black installed (pip3 install black)

3. Create a Feature Branch

4. (Recommended) Check whether your code conforms to our Coding Standards by running black on your changed files

5. Send us a Pull Request
