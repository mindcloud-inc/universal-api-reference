# Openlayer: List Framework Subsection Rules

Retrieves rules for a framework subsection in Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-framework-subsection-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-framework-subsection-rules?connectionId=$CONNECTION_ID&frameworkId=29e72db4-dd2f-4331-b1c4-d13b5160a404&subsectionId=fbaad985-d113-4463-9b9a-dde44f119a38" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "frameworkId": "29e72db4-dd2f-4331-b1c4-d13b5160a404",
  "subsectionId": "fbaad985-d113-4463-9b9a-dde44f119a38"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-framework-subsection-rules?${params}`, {
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
| `frameworkId` | string | yes | Openlayer framework ID. Default: `29e72db4-dd2f-4331-b1c4-d13b5160a404`. |
| `subsectionId` | string | yes | Openlayer framework subsection ID. Default: `fbaad985-d113-4463-9b9a-dde44f119a38`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_meta": {},
      "items": [
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
| `_meta` | object | Pagination metadata. |
| `items` | array<object> | Framework subsection rules. |

## Native endpoint

Through the native Openlayer API, this operation is `GET /frameworks/:frameworkId/subsections/:subsectionId/rules` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-framework-subsection-rules.md) for the provider-specific parameters and requirements.

