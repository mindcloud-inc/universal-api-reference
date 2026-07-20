# Crisp: Get People Data

Retrieves people data from Crisp.

```
GET https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-people-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crisp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-people-data?connectionId=$CONNECTION_ID&websiteId=string&peopleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "peopleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-people-data?${params}`, {
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
| `websiteId` | string | yes | The website identifier. |
| `peopleId` | string | yes | The people identifier or people email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Crisp API, this operation is `GET /website/:website_id/people/data/:people_id` (base URL `https://api.crisp.chat/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-people-data.md) for the provider-specific parameters and requirements.

