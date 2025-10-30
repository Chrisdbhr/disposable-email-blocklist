# Disposable Email Blocklist

A public, open-source, and curated list of disposable and temporary email domains. Ideal for developers looking to block fake sign-ups or spam in their applications.

The data is maintained in a simple `disposable_domains.txt` file and automatically generated into JSON and XML formats for easy consumption.

## 🚀 How to Use

You can consume this list directly via HTTP using the raw GitHub links below. For production environments, I highly recommend caching the results in your application to prevent issues if GitHub is unavailable.

* **TXT (Source of Truth)**
    ```
    https://raw.githubusercontent.com/Chrisdbhr/disposable-email-blocklist/master/disposable_domains.txt
    ```

* **JSON (Auto-Generated)**
    ```
    https://raw.githubusercontent.com/Chrisdbhr/disposable-email-blocklist/master/generated/disposable_domains.json
    ```

* **XML (Auto-Generated)**
    ```
    https://raw.githubusercontent.com/Chrisdbhr/disposable-email-blocklist/master/generated/disposable_domains.xml
    ```

### Data Formats

#### JSON
A simple array of strings.
```json
[
  "0-mail.com",
  "10minutemail.com",
  "1usemail.com",
  ...
]
```

#### XML
A root <domains> element containing multiple <domain> nodes.

```XML

<?xml version="1.0" encoding="UTF-8"?>
<domains>
  <domain>0-mail.com</domain>
  <domain>10minutemail.com</domain>
  <domain>1usemail.com</domain>
  ...
</domains>
```

## 🤝 How to Contribute
Contributions are very welcome!

- Fork this repository.
- Add your new domain(s) to the disposable_domains.txt file.
  - **IMPORTANT**: Only edit disposable_domains.txt. Do not manually edit the files in the generated/ folder.
  - Add one domain per line.
- Open a Pull Request.

Once your PR is merged, the GitHub Action will automatically run, validate, and update the JSON and XML files.

## 📄 License
This project is licensed under the MIT License. See the [LICENSE](https://github.com/Chrisdbhr/disposable-email-blocklist/blob/main/.github/LICENSE) file for details.
