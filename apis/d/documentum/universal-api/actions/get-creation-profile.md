# Documentum: Get Creation Profile



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-creation-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-creation-profile?connectionId=$CONNECTION_ID&repositoryName=d2repo&profileId=0900000180001234" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repositoryName": "d2repo",
  "profileId": "0900000180001234"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-creation-profile?${params}`, {
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
| `repositoryName` | string | yes | Documentum repository name. Example: `d2repo`. |
| `profileId` | string | yes | Object ID of the D2 creation profile. Example: `0900000180001234`. |

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
| `id` | string | Creation profile identifier. |
| `links[].href` | string | Profile link URL. |
| `links[].rel` | string | Profile link relation. |
| `title` | string | Creation profile title. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Documentum API, this operation is `GET /repositories/{repositoryName}/profile-configuration/{profileId}` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-creation-profile.md) for the provider-specific parameters and requirements.

