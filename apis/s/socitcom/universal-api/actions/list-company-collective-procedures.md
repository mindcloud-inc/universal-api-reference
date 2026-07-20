# Société.com: List Company Collective Procedures

Retrieves company collective procedures from Société.com.

```
GET https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/list-company-collective-procedures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Société.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/list-company-collective-procedures?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/list-company-collective-procedures?${params}`, {
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
| `numid` | string | no | Company identifier or SIREN. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "procedurescollectives": [
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
| `procedurescollectives` | array<object> | Collective procedure records associated with the company. |

## Native endpoint

Through the native Société.com API, this operation is `GET /entreprise/:numid/procedurescollectives` (base URL `https://api.societe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-collective-procedures.md) for the provider-specific parameters and requirements.

