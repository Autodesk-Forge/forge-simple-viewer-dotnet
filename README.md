# forge-simple-viewer-dotnet

> This is currently a work-in-progress.

Sample [Autodesk Forge](https://forge.autodesk.com) application attempting to provide a cleaner,
easier-to-read implementation of the "View Models" application from https://learnforge.autodesk.io.

## Setup & Run

- Clone this repository
- Install dependencies: `dotnet restore`
- Setup environment variables in the appsettings.Development.json (create this file if its missing):
  - `FORGE_CLIENT_ID` - your Forge application client ID
  - `FORGE_CLIENT_SECRET` - your Forge application client secret
  - `FORGE_BUCKET` - name of Forge bucket to store your designs in

```
Remember to replace the client ID, secret and forge bucket with your own. Note that the bucket name should be unique to your application.
Using a bucket name that is already in use with different forge app credentials (client Id and Secret) to upload a file will result in an error.
```


## Troubleshooting

### Invalid active developer path

If you're getting `invalid active developer path` errors, please follow the steps
explained in https://apple.stackexchange.com/questions/254380/why-am-i-getting-an-invalid-active-developer-path-when-attempting-to-use-git-a.

### Dev-certs errors

If you're seeing errors related to `dev-certs`, try cleaning any existing certificates
as explained in https://docs.microsoft.com/en-us/dotnet/core/additional-tools/self-signed-certificates-guide,
and on macOS and Windows systems, do not forget to use the `--trust` switch.
