# Odoo: Delete Job Positions

Deletes job positions from Odoo.

```
DELETE https://connect.mindcloud.co/v1/universal/odoo/latest/actions/delete-job-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Odoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/odoo/latest/actions/delete-job-positions?connectionId=$CONNECTION_ID&ids%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/odoo/latest/actions/delete-job-positions?${params}`, {
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
| `ids[]` | array<number> | yes | Array of Odoo job position IDs to delete as JSON. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Odoo API, this operation is `POST /hr.job/unlink` (base URL `https://{{credentials.domain}}/json/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-job-positions.md) for the provider-specific parameters and requirements.

