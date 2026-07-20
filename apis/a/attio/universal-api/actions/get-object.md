# Attio: Get Object

Retrieves an object from Attio.

```
GET https://connect.mindcloud.co/v1/universal/attio/latest/actions/get-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/attio/latest/actions/get-object?connectionId=$CONNECTION_ID&object=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "object": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/attio/latest/actions/get-object?${params}`, {
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
| `object` | string | yes | The Attio object slug or UUID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiSlug": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": {},
      "pluralNoun": "string",
      "singularNoun": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiSlug` | string | API slug for the object. |
| `createdAt` | date | When the object was created. |
| `id` | object | Object identifier payload containing workspace and object ids. |
| `pluralNoun` | string | Plural display name for the object. |
| `singularNoun` | string | Singular display name for the object. |

## Native endpoint

Through the native Attio API, this operation is `GET /v2/objects/:object` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-object.md) for the provider-specific parameters and requirements.

