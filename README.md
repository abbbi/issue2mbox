# issue2mbox

Export github issues as mbox file.

Setup:

```
python3 -m venv mbox
source mbox/bin/activate
pip3 install PyGithub
```

Create a access token for your account, call script via:

```issue2mbox -r <repository> -t <token>
[2022-02-21 11:32:14,278]    INFO  Exporting issues to [/tmp/issuelist]
[2022-02-21 11:32:14,448]    INFO  [2]: [second issue] Comments: [2]
[2022-02-21 11:32:14,608]    INFO  [1]: [bla issue 1] Comments: [1]
```

Issues and related comments will be exported as mbox
file, can be opened via mutt:

```
tree /tmp/issuelist/
/tmp/issuelist/
├── 1.mbox
└── 2.mbox
```

Now read the issues using mutt:

`# mutt -f /tmp/issuelist/1.mbox`
