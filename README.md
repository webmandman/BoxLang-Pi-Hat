# BoxLang Pi Hat

The quickest and simplest way to get up and running on this is to download and install CommandBox.

https://www.ortussolutions.com/products/commandbox

Then follow the steps below:

* Fork the repo
* Clone the repo locally <code>git clone {{repo_url}}</code>
* cd into the directory
* Run the following command: <code>box server start</code>
* Access the URL given in the terminal when the server starts e.g. 127.0.0.1:50443

## Emulator

This project has en emulator to help you test and run your animations before contributing back to the project.

See the README.md in the <code>/emulator</code> folder for details

The service to auto-start this is located at `/etc/systemd/system/boxlang.service` with the following contents:

```
[Unit]
Description=BoxLang MatrixRunner Service

[Service]
User=root
WorkingDirectory=/home/brad/BoxLang-Pi-Hat
ExecStart=boxlang MatrixRunner.bx
Restart=always
RestartSec=5
StandardOutput=journal
StandardError=journal

[Install]
WantedBy=multi-user.target
```
