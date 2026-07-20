# Xperiencify: Get Student Info

Retrieves student details from Xperiencify by email address.

```
GET https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/get-student-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xperiencify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/get-student-info?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/get-student-info?${params}`, {
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
| `email` | string | yes | Student email address. |
| `courseId` | number | no | Optional course context for course-specific progress data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstName": "Ava",
      "globalXpEarned": 1,
      "globalXpPercComplete": 1,
      "globalXpTotal": 1,
      "globalXxpEarned": 1,
      "globalXxpPercComplete": 1,
      "globalXxpTotal": 1,
      "id": 1,
      "lastName": "Chen",
      "phone": "string",
      "tags": [
        "string"
      ],
      "xpEarned": 1,
      "xpPercComplete": 1,
      "xpTotal": 1,
      "xxpEarned": 1,
      "xxpPercComplete": 1,
      "xxpTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Student email address. |
| `firstName` | string | Student first name. |
| `globalXpEarned` | number | Aggregate XP earned when courseId is omitted. |
| `globalXpPercComplete` | number | Aggregate XP completion percentage when courseId is omitted. |
| `globalXpTotal` | number | Aggregate total XP when courseId is omitted. |
| `globalXxpEarned` | number | Aggregate XXP earned when courseId is omitted. |
| `globalXxpPercComplete` | number | Aggregate XXP completion percentage when courseId is omitted. |
| `globalXxpTotal` | number | Aggregate total XXP when courseId is omitted. |
| `id` | number | Student identifier. |
| `lastName` | string | Student last name. |
| `phone` | string | Student phone number. |
| `tags` | array<string> | Student tags. |
| `xpEarned` | number | Course-specific XP earned when courseId is provided. |
| `xpPercComplete` | number | Course-specific XP completion percentage when courseId is provided. |
| `xpTotal` | number | Course-specific total XP when courseId is provided. |
| `xxpEarned` | number | Course-specific XXP earned when courseId is provided. |
| `xxpPercComplete` | number | Course-specific XXP completion percentage when courseId is provided. |
| `xxpTotal` | number | Course-specific total XXP when courseId is provided. |

## Native endpoint

Through the native Xperiencify API, this operation is `POST /api/public/student/info/` (base URL `https://api.xperiencify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-student-info.md) for the provider-specific parameters and requirements.

