# Document360: List Version Languages



```
GET https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-version-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-version-languages?connectionId=$CONNECTION_ID&projectVersionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectVersionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-version-languages?${params}`, {
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
| `projectVersionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countryFlagCode": "string",
      "isSetAsDefault": true,
      "languageCode": "string",
      "languageId": "string",
      "languageName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryFlagCode` | string |  |
| `isSetAsDefault` | boolean |  |
| `languageCode` | string |  |
| `languageId` | string |  |
| `languageName` | string |  |

## Native endpoint

Through the native Document360 API, this operation is `GET /v2/Language/:projectVersionId` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-version-languages.md) for the provider-specific parameters and requirements.

