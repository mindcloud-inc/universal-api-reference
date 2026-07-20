# Porsline: List Survey Authentication Codes



```
GET https://connect.mindcloud.co/v1/universal/porsline/latest/actions/list-survey-authentication-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/list-survey-authentication-codes?connectionId=$CONNECTION_ID&survey_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "survey_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/porsline/latest/actions/list-survey-authentication-codes?${params}`, {
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
| `survey_id` | number | yes | The id of the target survey. |
| `page` | number | no | Page number. |
| `pageSize` | number | no | Maximum number of authentication codes to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Total authentication code count. |
| `next` | string | Next page URL when present. |
| `previous` | string | Previous page URL when present. |
| `results` | array<string> | Authentication codes returned by Porsline. |

## Native endpoint

Through the native Porsline API, this operation is `GET /api/surveys/:survey_id/settings/authentication-codes/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-survey-authentication-codes.md) for the provider-specific parameters and requirements.

