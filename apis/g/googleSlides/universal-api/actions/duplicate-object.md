# Google Slides: Duplicate Object

Duplicates a slide or page element. A duplicated slide is placed right after the original; a duplicated element stays on the same slide.

```
POST https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/duplicate-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Slides `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/duplicate-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "presentationId": "string",
  "objectId": "p"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/duplicate-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "presentationId": "string",
    "objectId": "p"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `presentationId` | list<string> | yes | The ID of the presentation to update. |
| `objectId` | string | yes | Object ID of the slide or page element to duplicate. Example: `p`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectIds` | object | no | Map of original object IDs to the IDs to use for the duplicates, for example {"p": "slideCopy_01"}. Unmapped objects get random IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "replies": [
        {
          "duplicateObject": {
            "objectId": "string"
          }
        }
      ],
      "presentationId": "string",
      "writeControl": {
        "requiredRevisionId": "string"
      },
      "commentUpdateState": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `replies[].duplicateObject.objectId` | string | Object ID of the duplicate. |
| `presentationId` | string | The ID of the presentation that was updated. |
| `writeControl.requiredRevisionId` | string | Revision ID of the presentation after the update, usable for conditional writes. |
| `commentUpdateState` | string | Whether the request changed comments. |

## Native endpoint

Through the native Google Slides API, this operation is `POST /v1/presentations/[:presentationId]\:batchUpdate` (base URL `https://slides.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-object.md) for the provider-specific parameters and requirements.

