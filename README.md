### Java 17 lib for srcclr scan

In order to scan the library, run the following commands after adding in your api token:
```bash
export SRCCLR_API_TOKEN=<your-token-here>
curl -sSL https://download.sourceclear.com/ci.sh | bash -s scan . \
--scan-collectors maven --allow-dirty --update-advisor --no-upload --debug
```
or with custom JDK (where env var JAVA_HOME points to your JDK 17 home dir)
```bash
export SRCCLR_API_TOKEN=<your-token-here>
curl -sSL https://download.sourceclear.com/ci.sh | CUSTOM_JRE_DIR=$JAVA_HOME bash -s scan . \
--scan-collectors maven --allow-dirty --update-advisor --no-upload --debug
```