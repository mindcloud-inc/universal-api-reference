# Update Policy Tags with Expensify

Updates policy tags in Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Update Policy Tags](https://integrations.expensify.com/Integration-Server/doc/#update-tags-nbsp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyId` | body | `string` | yes | The Expensify policy ID to update. |
| `tagsJson` | body | `string` | yes | JSON array of tag-level objects, for example [{"name":"Team","tags":[{"name":"Sales"}]}]. |
