# Zoho Recruit: Delete Records

Deletes records from a Zoho Recruit module.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/delete-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/delete-records?connectionId=$CONNECTION_ID&moduleApiName=Ava%20Chen&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moduleApiName": "Ava Chen",
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/delete-records?${params}`, {
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
| `moduleApiName` | string | yes | The Zoho Recruit module API name whose records you want to delete. |
| `ids` | string | yes | A comma-separated list of Zoho Recruit record IDs to delete. Accepts multiple values in one string, delimited by `,`. |
| `wfTrigger` | boolean | no | Whether to trigger workflows when the records are deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "details": {},
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `details` | object |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Recruit API, this operation is `DELETE /:moduleApiName` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-records.md) for the provider-specific parameters and requirements.

