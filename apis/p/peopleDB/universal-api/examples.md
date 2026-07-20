# PeopleDB Universal API Examples

These examples use the MindCloud API key and PeopleDB connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contact Info by GitHub Username

Retrieves contact info from PeopleDB by GitHub username.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDB/latest/actions/get-contact-info-by-git-hub-username?connectionId=$CONNECTION_ID&githubLogin=e.g.%20dhh" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "githubLogin": "e.g. dhh"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peopleDB/latest/actions/get-contact-info-by-git-hub-username?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "emailAddresses": [
        "ava@example.com"
      ],
      "facebookUsername": "Ava Chen",
      "githubId": 1,
      "githubLogin": "string",
      "githubUsername": "Ava Chen",
      "linkedinId": 1,
      "linkedinPublicIdentifier": "https://example.com",
      "personalEmailAddresses": [
        "ava@example.com"
      ],
      "phoneNumbers": [
        "string"
      ],
      "twitterUsername": "Ava Chen",
      "workEmailAddresses": [
        "ava@example.com"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Contact Info by GitHub Username action reference](actions/get-contact-info-by-git-hub-username.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/peopleDB/latest/actions/get-contact-info-by-git-hub-username).

## Validate Email Address via POST

Validates an email address in PeopleDB via POST.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/peopleDB/latest/actions/validate-email-address-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailAddress": "e.g. user@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peopleDB/latest/actions/validate-email-address-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailAddress": "e.g. user@example.com"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "checks": {},
      "classification": "string",
      "email": "ava@example.com",
      "errors": [
        "string"
      ],
      "score": 1,
      "scoreDetails": {},
      "valid": true,
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Validate Email Address via POST action reference](actions/validate-email-address-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/peopleDB/latest/actions/validate-email-address-post).
