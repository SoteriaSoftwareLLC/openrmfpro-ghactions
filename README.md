# openrmfpro-ghactions
OpenRMF Professional public repo to show how to handle files and API interactions via GitHub Actions


## Get a list of files

https://stackoverflow.com/questions/74854189/call-external-rest-api-when-a-file-is-added-or-updated-to-a-github-repository

https://github.com/marketplace/actions/changed-files

https://github.com/marketplace/actions/changed-files


## Do something with them 

https://github.com/fjogeleit/http-request-action/blob/main/.github/workflows/ci.yml

https://github.com/fjogeleit/http-request-action/

```
https://{root-url}/api/external/systempackage/{systemKey}/scapchecklist/?applicationKey={applicationKey}

formdata:
  checklistFile *.xml/*.ckl/*.nessus/*.csv

Authorization Token is the Bearer, space, then the API Token
```

## Files are in directories to keep them separate

You can get a list of all files, all files in a directory, all files by directory, etc. and process as required