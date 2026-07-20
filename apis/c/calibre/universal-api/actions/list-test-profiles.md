# Calibre: List Test Profiles

Retrieves test profiles for a site from Calibre.

```
GET https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-test-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-test-profiles?connectionId=$CONNECTION_ID&variables.site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-test-profiles?${params}`, {
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
| `variables.site` | string | yes | Site slug, found in site settings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organisation": {
        "site": {
          "testProfiles": [
            {
              "adBlockerIsEnabled": true,
              "bandwidth": {
                "tag": "string",
                "title": "string"
              },
              "createdAt": "2026-05-07T12:00:00.000Z",
              "device": {
                "tag": "string",
                "title": "string"
              },
              "jsIsDisabled": true,
              "name": "Ava Chen",
              "position": 1,
              "updatedAt": "2026-05-07T12:00:00.000Z",
              "uuid": "string"
            }
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organisation.site.testProfiles[].adBlockerIsEnabled` | boolean |  |
| `organisation.site.testProfiles[].bandwidth.tag` | string |  |
| `organisation.site.testProfiles[].bandwidth.title` | string |  |
| `organisation.site.testProfiles[].createdAt` | date |  |
| `organisation.site.testProfiles[].device.tag` | string |  |
| `organisation.site.testProfiles[].device.title` | string |  |
| `organisation.site.testProfiles[].jsIsDisabled` | boolean |  |
| `organisation.site.testProfiles[].name` | string |  |
| `organisation.site.testProfiles[].position` | number |  |
| `organisation.site.testProfiles[].updatedAt` | date |  |
| `organisation.site.testProfiles[].uuid` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-test-profiles.md) for the provider-specific parameters and requirements.

