# Digit.ink: Get Credential Stack



```
GET https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-credential-stack
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digit.ink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-credential-stack?connectionId=$CONNECTION_ID&credentialUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "credentialUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitink/latest/actions/get-credential-stack?${params}`, {
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
| `credentialUuid` | string | yes | Credential UUID path parameter. |
| `password` | string | no | Optional credential password query parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chain": "string",
      "credentialJsonUrl": "https://example.com",
      "credentialSubject": {},
      "credentialTitle": "string",
      "credentialType": "string",
      "credentialUuid": "string",
      "credentialVersion": "string",
      "currentStatus": "string",
      "id": "string",
      "isAddToLinkedInButtonShown": true,
      "isArchived": true,
      "isProfileAndDescriptionShown": true,
      "issued": "2026-05-07T12:00:00.000Z",
      "issuerUri": "string",
      "linkedCredentials": [
        {}
      ],
      "lmsUserId": "string",
      "mailingAddress": {},
      "password": "string",
      "printShipReqCount": 1,
      "productKey": "string",
      "shareSettings": {},
      "stackName": "Ava Chen",
      "templateName": "Ava Chen",
      "templateUuid": "string",
      "validFrom": "2026-05-07T12:00:00.000Z",
      "validUntil": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chain` | string |  |
| `credentialJsonUrl` | string |  |
| `credentialSubject` | object |  |
| `credentialTitle` | string |  |
| `credentialType` | string |  |
| `credentialUuid` | string |  |
| `credentialVersion` | string |  |
| `currentStatus` | string |  |
| `id` | string |  |
| `isAddToLinkedInButtonShown` | boolean |  |
| `isArchived` | boolean |  |
| `isProfileAndDescriptionShown` | boolean |  |
| `issued` | date |  |
| `issuerUri` | string |  |
| `linkedCredentials` | array<object> |  |
| `lmsUserId` | string |  |
| `mailingAddress` | object |  |
| `password` | string |  |
| `printShipReqCount` | number |  |
| `productKey` | string |  |
| `shareSettings` | object |  |
| `stackName` | string |  |
| `templateName` | string |  |
| `templateUuid` | string |  |
| `validFrom` | date |  |
| `validUntil` | date |  |

## Native endpoint

Through the native Digit.ink API, this operation is `GET /credentials/:credentialUuid/stack` (base URL `https://app.digit.ink/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credential-stack.md) for the provider-specific parameters and requirements.

