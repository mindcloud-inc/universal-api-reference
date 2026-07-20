# Hireflix: Get Position Public Submission Settings

Retrieves public submission settings for a position in Hireflix.

```
GET https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-position-public-submission-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-position-public-submission-settings?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-position-public-submission-settings?${params}`, {
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
| `variables.id` | string | yes | The Hireflix position ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow": true,
      "phoneNumberHidden": true,
      "phoneNumberRequired": true,
      "url": "https://example.com",
      "verifyEmail": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow` | boolean |  |
| `phoneNumberHidden` | boolean |  |
| `phoneNumberRequired` | boolean |  |
| `url` | string |  |
| `verifyEmail` | boolean |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-position-public-submission-settings.md) for the provider-specific parameters and requirements.

