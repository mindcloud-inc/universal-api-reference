# Refiner: Duplicate Form

Creates a duplicate of a form in Refiner.

```
POST https://connect.mindcloud.co/v1/universal/refiner/latest/actions/duplicate-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refiner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/duplicate-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formUuid": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refiner/latest/actions/duplicate-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formUuid": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formUuid` | string | yes | The source form UUID to duplicate. |
| `name` | string | yes | Name to assign to the duplicated draft form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "newFormUuid": "string",
      "sourceFormUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `newFormUuid` | string |  |
| `sourceFormUuid` | string |  |

## Native endpoint

Through the native Refiner API, this operation is `POST /forms/duplicate` (base URL `https://api.refiner.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-form.md) for the provider-specific parameters and requirements.

