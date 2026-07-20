# Codeberg: Get Current User Quota



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-current-user-quota
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-current-user-quota?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-current-user-quota?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "groups": [
        {
          "name": "Ava Chen",
          "rules": [
            {
              "limit": 1,
              "name": "Ava Chen",
              "subjects": [
                "string"
              ]
            }
          ]
        }
      ],
      "used": {
        "size": {
          "assets": {
            "artifacts": 1,
            "attachments": {
              "issues": 1,
              "releases": 1
            },
            "packages": {
              "all": 1
            }
          },
          "git": {
            "lfs": 1
          },
          "repos": {
            "public": 1
          }
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
| `groups[].name` | string |  |
| `groups[].rules[].limit` | number |  |
| `groups[].rules[].name` | string |  |
| `groups[].rules[].subjects` | array<string> |  |
| `used.size.assets.artifacts` | number |  |
| `used.size.assets.attachments.issues` | number |  |
| `used.size.assets.attachments.releases` | number |  |
| `used.size.assets.packages.all` | number |  |
| `used.size.git.lfs` | number |  |
| `used.size.repos.public` | number |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user/quota` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-quota.md) for the provider-specific parameters and requirements.

