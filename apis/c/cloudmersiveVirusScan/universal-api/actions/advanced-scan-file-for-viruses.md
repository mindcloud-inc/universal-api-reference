# Cloudmersive Virus Scan: Advanced Scan File for Viruses

Performs an advanced file virus scan with Cloudmersive Virus Scan.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveVirusScan/latest/actions/advanced-scan-file-for-viruses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Virus Scan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveVirusScan/latest/actions/advanced-scan-file-for-viruses?connectionId=$CONNECTION_ID&inputFile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputFile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveVirusScan/latest/actions/advanced-scan-file-for-viruses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputFile` | file | yes | Input file to scan for viruses and advanced content threats. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CleanResult": true,
      "ContainsExecutable": true,
      "ContainsHtml": true,
      "ContainsInsecureDeserialization": true,
      "ContainsInvalidFile": true,
      "ContainsMacros": true,
      "ContainsOleEmbeddedObject": true,
      "ContainsPasswordProtectedFile": true,
      "ContainsRestrictedFileFormat": true,
      "ContainsScript": true,
      "ContainsUnsafeArchive": true,
      "ContainsUnwantedAction": true,
      "ContainsXmlExternalEntities": true,
      "ContentInformation": {
        "ContainsImage": true,
        "ContainsJSON": true,
        "ContainsXML": true,
        "Hash_SHA1": "string",
        "IsAuthenticodeSigned": true,
        "RelevantSubfileHash_SHA1": "string",
        "RelevantSubfileName": "Ava Chen"
      },
      "FoundViruses": [
        {
          "FileName": "Ava Chen",
          "VirusName": "Ava Chen"
        }
      ],
      "VerifiedFileFormat": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CleanResult` | boolean | True when Cloudmersive found no viruses or advanced content threats. |
| `ContainsExecutable` | boolean | True when the file contains executable code. |
| `ContainsHtml` | boolean | True when the input contains HTML. |
| `ContainsInsecureDeserialization` | boolean | True when the input contains insecure deserialization threats. |
| `ContainsInvalidFile` | boolean | True when the input contains an invalid file. |
| `ContainsMacros` | boolean | True when the input contains document macros. |
| `ContainsOleEmbeddedObject` | boolean | True when the input contains an OLE embedded object. |
| `ContainsPasswordProtectedFile` | boolean | True when the input contains password protected or encrypted files. |
| `ContainsRestrictedFileFormat` | boolean | True when the file type is not allowed by the optional restrictFileTypes setting. |
| `ContainsScript` | boolean | True when the input contains script content. |
| `ContainsUnsafeArchive` | boolean | True when the input contains unsafe archive content. |
| `ContainsUnwantedAction` | boolean | True when the input contains an unwanted automatic action. |
| `ContainsXmlExternalEntities` | boolean | True when the input contains XML External Entity threats. |
| `ContentInformation` | object | Additional non-threat content verification information. |
| `ContentInformation.ContainsImage` | boolean | True when the input file contains image data. |
| `ContentInformation.ContainsJSON` | boolean | True when the input file contains JSON data. |
| `ContentInformation.ContainsXML` | boolean | True when the input file contains XML data. |
| `ContentInformation.Hash_SHA1` | string | SHA1 hash of the input file. |
| `ContentInformation.IsAuthenticodeSigned` | boolean | True when there is a valid Authenticode signature. |
| `ContentInformation.RelevantSubfileHash_SHA1` | string | SHA1 hash of the relevant subfile in an archive, if any. |
| `ContentInformation.RelevantSubfileName` | string | Relevant subfile name in an archive for identified threats, if any. |
| `FoundViruses` | array<object> | Viruses found in the scanned file, when any are detected. |
| `FoundViruses[].FileName` | string | File name where the virus was found. |
| `FoundViruses[].VirusName` | string | Detected virus or malware name. |
| `VerifiedFileFormat` | string | Detected and verified file format. |

## Native endpoint

Through the native Cloudmersive Virus Scan API, this operation is `POST /virus/scan/file/advanced` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/advanced-scan-file-for-viruses.md) for the provider-specific parameters and requirements.

