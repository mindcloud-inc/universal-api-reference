# Recommand: Verify Recipient

Verifies a recipient in the Recommand directory.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/verify-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/verify-recipient?connectionId=$CONNECTION_ID&limit=25&offset=0&peppoladdress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "peppoladdress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/verify-recipient?${params}`, {
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
| `includebusinesscard` | boolean | no | If true, fetches the business card from the SMP for company name and country. |
| `includeendpointdetails` | boolean | no | If true, fetches endpoint details for all supported document types. |
| `peppoladdress` | string | yes | The Peppol address of the recipient to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "countryCode": "string",
      "isValid": true,
      "serviceMetadataReferences": [
        "string"
      ],
      "smpHostnames": [
        "Ava Chen"
      ],
      "smpUrl": "https://example.com",
      "success": true,
      "supportedDocuments": [
        {
          "certificateExpiry": "string",
          "docTypeId": "string",
          "name": "Ava Chen",
          "serviceEndpoint": "string",
          "serviceProvider": "string",
          "technicalContact": "string"
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
| `companyName` | string |  |
| `countryCode` | string |  |
| `isValid` | boolean |  |
| `serviceMetadataReferences` | array<string> |  |
| `smpHostnames` | array<string> |  |
| `smpUrl` | string |  |
| `success` | boolean |  |
| `supportedDocuments` | array<object> |  |
| `supportedDocuments[].certificateExpiry` | string |  |
| `supportedDocuments[].docTypeId` | string |  |
| `supportedDocuments[].name` | string |  |
| `supportedDocuments[].serviceEndpoint` | string |  |
| `supportedDocuments[].serviceProvider` | string |  |
| `supportedDocuments[].technicalContact` | string |  |

## Native endpoint

Through the native Recommand API, this operation is `POST /api/v1/verify` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/verify-recipient.md) for the provider-specific parameters and requirements.

