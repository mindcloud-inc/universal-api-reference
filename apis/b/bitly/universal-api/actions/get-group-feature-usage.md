# Bitly: Get Group Feature Usage

Retrieves feature usage for a Bitly group.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-group-feature-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-group-feature-usage?connectionId=$CONNECTION_ID&groupGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-group-feature-usage?${params}`, {
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
| `groupGuid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupGuid": "string",
      "limitUsage": [
        {
          "count": 1,
          "description": "string",
          "name": "Ava Chen"
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
| `groupGuid` | string |  |
| `limitUsage[].count` | number |  |
| `limitUsage[].description` | string |  |
| `limitUsage[].name` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /groups/:group_guid/feature_usage` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group-feature-usage.md) for the provider-specific parameters and requirements.

