# Cloudmersive Virus Scan: Scan File for Viruses

Scans a file for viruses with Cloudmersive Virus Scan.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveVirusScan/latest/actions/scan-file-for-viruses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Virus Scan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveVirusScan/latest/actions/scan-file-for-viruses?connectionId=$CONNECTION_ID&inputFile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputFile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveVirusScan/latest/actions/scan-file-for-viruses?${params}`, {
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
| `inputFile` | file | yes | Input file to scan for viruses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CleanResult": true,
      "FoundViruses": [
        {
          "FileName": "Ava Chen",
          "VirusName": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CleanResult` | boolean | True when Cloudmersive found no virus in the scanned file. |
| `FoundViruses` | array<object> | Viruses found in the scanned file, when any are detected. |
| `FoundViruses[].FileName` | string | File name where the virus was found. |
| `FoundViruses[].VirusName` | string | Detected virus or malware name. |

## Native endpoint

Through the native Cloudmersive Virus Scan API, this operation is `POST /virus/scan/file` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scan-file-for-viruses.md) for the provider-specific parameters and requirements.

