# ShareFile: Get Share



```
GET https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-share
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShareFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-share?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-share?${params}`, {
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
| `id` | string | yes | The ShareFile share identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AliasID": "string",
      "CreationDate": "string",
      "ExpirationDate": "string",
      "HasSentMessage": true,
      "Id": "string",
      "IsPersistentLink": true,
      "IsViewOnly": true,
      "MaxDownloads": 1,
      "odata": {
        "metadata": "string",
        "type": "string"
      },
      "RequireLogin": true,
      "ShareAccessLevel": "string",
      "ShareAccessRight": {},
      "ShareSubType": "string",
      "ShareType": "string",
      "Title": "string",
      "TotalDownloads": 1,
      "Uri": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AliasID` | string | The ShareFile public alias identifier for the share. |
| `CreationDate` | string | The share creation timestamp. |
| `ExpirationDate` | string | The share expiration timestamp. |
| `HasSentMessage` | boolean | Whether the share has a sent message. |
| `Id` | string | The ShareFile share identifier. |
| `IsPersistentLink` | boolean | Whether the share is a persistent link. |
| `IsViewOnly` | boolean | Whether the share is view-only. |
| `MaxDownloads` | number | The maximum allowed downloads. |
| `odata.metadata` | string | The OData metadata URL for the returned share. |
| `odata.type` | string | The OData type for the returned share. |
| `RequireLogin` | boolean | Whether the share requires login. |
| `ShareAccessLevel` | string | The ShareFile access level for the share. |
| `ShareAccessRight` | object | The effective access rights for the share. |
| `ShareSubType` | string | The ShareFile share subtype. |
| `ShareType` | string | The ShareFile share type. |
| `Title` | string | The share title. |
| `TotalDownloads` | number | The total recorded downloads. |
| `Uri` | string | The share URL. |
| `url` | string | The API URL for the returned share. |

## Native endpoint

Through the native ShareFile API, this operation is `GET /Shares({{id}})` (base URL `https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/sf/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-share.md) for the provider-specific parameters and requirements.

