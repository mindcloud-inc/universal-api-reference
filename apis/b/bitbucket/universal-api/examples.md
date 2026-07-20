# Bitbucket Universal API Examples

These examples use the MindCloud API key and Bitbucket connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Workspace

Retrieves a workspace from Bitbucket.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspace=mindcloudbitbucket20260409" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace": "mindcloudbitbucket20260409"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-workspace?${params}`, {
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
      "is_private": true,
      "name": "Ava Chen",
      "slug": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Workspace action reference](actions/get-workspace.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bitbucket/latest/actions/get-workspace).

## Create Or Update Repository

Creates or updates a repository in Bitbucket.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/create-or-update-repository" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace": "string",
  "repo_slug": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/create-or-update-repository', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace": "string",
    "repo_slug": "string",
    "name": "Ava Chen"
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
      "description": "string",
      "full_name": "Ava Chen",
      "is_private": true,
      "language": "string",
      "name": "Ava Chen",
      "slug": "string",
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Or Update Repository action reference](actions/create-or-update-repository.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bitbucket/latest/actions/create-or-update-repository).
