# leadtributor.cloud: Get Lead

Retrieves a lead from leadtributor.cloud.

```
GET https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a leadtributor.cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/get-lead?connectionId=$CONNECTION_ID&leadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/get-lead?${params}`, {
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
| `leadId` | string | yes | ID of the lead to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "interest": {
        "fieldOrder": [
          "string"
        ],
        "fields": {},
        "required": [
          "string"
        ]
      },
      "prospect": {
        "fieldOrder": [
          "string"
        ],
        "fields": {},
        "required": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `interest.fieldOrder` | array<string> | Display order of interest fields. |
| `interest.fields` | object | Interest field definitions and values. |
| `interest.required` | array<string> | Required interest field keys. |
| `prospect.fieldOrder` | array<string> | Display order of prospect fields. |
| `prospect.fields` | object | Prospect field definitions and values. |
| `prospect.required` | array<string> | Required prospect field keys. |

## Native endpoint

Through the native leadtributor.cloud API, this operation is `GET /leads/:leadId` (base URL `https://api.leadtributor.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

