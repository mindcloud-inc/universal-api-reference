# 123FormBuild Universal API Examples

These examples use the MindCloud API key and 123FormBuild connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Forms

Retrieves forms from your 123FormBuilder account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/list-forms?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Forms action reference](actions/list-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formBuild/latest/actions/list-forms).

## Create Account

Creates a new account in 123FormBuilder when available for your account.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "password": "string",
  "passwordRepeat": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "password": "string",
    "passwordRepeat": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Account action reference](actions/create-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formBuild/latest/actions/create-account).
