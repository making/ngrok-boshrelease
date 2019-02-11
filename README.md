# ngrok bosh release


```
bosh create-release --name=ngrok --force --timestamp-version --tarball=/tmp/ngrok-boshrelease.tgz && bosh upload-release /tmp/ngrok-boshrelease.tgz 
bosh -n -d ngrok deploy manifest/demo.yml -v authtoken=$(bosh int ~/.ngrok2/ngrok.yml --path /authtoken) --no-redact
```