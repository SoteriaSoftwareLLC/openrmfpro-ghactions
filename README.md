# openrmfpro-ghactions
OpenRMF Professional public repo to show how to handle files and API interactions via GitHub Actions.

You can use GitHub Actions to process new/changed files in a GitHub repository and automatically push to OpenRMF Professional for tracking your cyber compliance. If you use GitHub for storing scan results for your ATO or accreditation package such asCKL, SCAP XML, you can easily enable automated ingest into OpenRMF Professional. Do the same for compliance statements, hardware, software, PPSM, mitigation statements and other lists to use for OpenRMF Professional with this simple workflow.

https://dale-bingham-soteriasoftware.medium.com/using-github-actions-and-the-openrmf-professional-api-for-automating-cyber-compliance-c4a174c78163 

## Get a list of files

Used a GH action from the marketplace to list changed files easily.

> DO NOT USE SPACES IN FILENAMES

https://stackoverflow.com/questions/74854189/call-external-rest-api-when-a-file-is-added-or-updated-to-a-github-repository

https://github.com/marketplace/actions/changed-files


## Do something with them 

For us, we posted them to OpenRMF Professional via a simple `curl` command using the server, system package, application key and api token for our calls. 

An example URL for the checklist/SCAP upload is below with relevant information:

```
https://{root-url}/api/external/systempackage/{systemKey}/scapchecklist/?applicationKey={applicationKey}

formdata:
  checklistFile *.xml/*.ckl/*.nessus/*.csv

Authorization Token is the Bearer, space, then the API Token
```

## Files are in directories to keep them separate

You can get a list of all files, all files in a directory, all files by directory, etc. and process as required.

We used simple named files but you can do this any way you wish.