# Deepgram: Get Project Billing Breakdown

Retrieves a project billing breakdown from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-billing-breakdown
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-billing-breakdown?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-billing-breakdown?${params}`, {
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
| `projectId` | string | yes | Deepgram project identifier. |
| `start` | string | no | Start date of the requested billing range in YYYY-MM-DD format. |
| `end` | string | no | End date of the requested billing range in YYYY-MM-DD format. |
| `accessor` | string | no | Filter billing breakdown rows by accessor identifier. |
| `deployment` | string | no | Filter billing breakdown rows by deployment: hosted, beta, or self-hosted. |
| `tag` | string | no | Filter billing breakdown rows by a specific tag. |
| `lineItem` | string | no | Filter billing breakdown rows by line item, for example streaming::nova-3. |
| `grouping` | string | no | Grouping dimensions encoded as a JSON-style list string, for example ["deployment","line_item"]. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "string",
      "resolution": {},
      "results": [
        {}
      ],
      "start": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | string | End date of the billing summary period. |
| `resolution` | object | Resolution metadata for the billing summary. |
| `results` | array<object> | Grouped billing breakdown rows. |
| `start` | string | Start date of the billing summary period. |

## Native endpoint

Through the native Deepgram API, this operation is `GET /v1/projects/:project_id/billing/breakdown` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-billing-breakdown.md) for the provider-specific parameters and requirements.

