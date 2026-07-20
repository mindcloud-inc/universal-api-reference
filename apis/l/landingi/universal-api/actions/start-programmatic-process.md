# Landingi: Start Programmatic Process

Starts a programmatic landing page process in Landingi.

```
POST https://connect.mindcloud.co/v1/universal/landingi/latest/actions/start-programmatic-process
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landingi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/landingi/latest/actions/start-programmatic-process" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceLandingPageUuid": "string",
  "name": "Ava Chen",
  "immediatePublication": true,
  "variants[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/landingi/latest/actions/start-programmatic-process', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceLandingPageUuid": "string",
    "name": "Ava Chen",
    "immediatePublication": true,
    "variants[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceLandingPageUuid` | string | yes | UUID of the source landing page. |
| `name` | string | yes | Name of the process. |
| `immediatePublication` | boolean | yes | Whether to publish the landing pages immediately. |
| `destinationGroupName` | string | no | Name of the group to assign the landing pages to. |
| `variants[]` | array<object> | yes | Programmatic landing page data. |
| `variants[].name` | string | no | Name of the programmatic landing page. |
| `variants[].domainUrl` | string | no | Full domain URL of the landing page. |
| `variants[].placeholders[]` | array<object> | no | Placeholder values for the landing page. |
| `variants[].placeholders[].key` | string | no | Placeholder content key. |
| `variants[].placeholders[].value` | string | no | Value used to replace the placeholder. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "process_identifier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `process_identifier` | string | Identifier of the created programmatic process. |

## Native endpoint

Through the native Landingi API, this operation is `POST /landing-page/programmatic/start` (base URL `https://api.landingi.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-programmatic-process.md) for the provider-specific parameters and requirements.

