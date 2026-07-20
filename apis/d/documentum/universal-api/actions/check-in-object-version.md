# Documentum: Check In Object Version



```
PUT https://connect.mindcloud.co/v1/universal/documentum/latest/actions/check-in-object-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/check-in-object-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "repositoryName": "d2repo",
  "chronicleId": "090000018000ffff",
  "objectId": "090000018000abcd",
  "versionPolicy": "next-minor"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentum/latest/actions/check-in-object-version', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "repositoryName": "d2repo",
    "chronicleId": "090000018000ffff",
    "objectId": "090000018000abcd",
    "versionPolicy": "next-minor"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `repositoryName` | string | yes | Documentum repository name. Example: `d2repo`. |
| `chronicleId` | string | yes | Chronicle ID of the object being checked in. Example: `090000018000ffff`. |
| `objectId` | string | yes | Current object ID being checked in. Example: `090000018000abcd`. |
| `versionPolicy` | string | yes | Versioning policy: next-major, next-minor, branch-version, or same-version. Example: `next-minor`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties` | object | no | Optional JSON properties payload for the check-in. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "links": [
        {
          "href": "https://example.com",
          "rel": "https://example.com"
        }
      ],
      "properties": {
        "objectName": "Ava Chen",
        "versionLabel": "string"
      },
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Versioned object identifier. |
| `links[].href` | string | Object link URL. |
| `links[].rel` | string | Object link relation. |
| `properties.objectName` | string | Object name. |
| `properties.versionLabel` | string | Version label. |
| `title` | string | Object title. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Documentum API, this operation is `POST /repositories/{repositoryName}/objects/{chronicleId}/versions` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-in-object-version.md) for the provider-specific parameters and requirements.

