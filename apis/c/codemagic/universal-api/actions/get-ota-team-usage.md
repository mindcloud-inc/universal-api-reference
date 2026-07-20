# Codemagic: Get OTA Team Usage

Retrieves over-the-air update usage for a Codemagic team.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-ota-team-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-ota-team-usage?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-ota-team-usage?${params}`, {
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
| `teamId` | string | yes | Codemagic team identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `periodFrom` | date | no | Optional usage-period start timestamp or date. |
| `periodTo` | date | no | Optional usage-period end timestamp or date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "series": [
        {}
      ],
      "summary": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object |  |
| `series` | array<object> |  |
| `summary` | array<object> |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/over-the-air-updates/:team_id/usage` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ota-team-usage.md) for the provider-specific parameters and requirements.

