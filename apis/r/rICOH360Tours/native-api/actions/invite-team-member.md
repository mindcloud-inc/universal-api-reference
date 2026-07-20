# Invite Team Member with RICOH360 Tours

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://bbomwcm27nhalfwjvwzy6qbrim.appsync-api.us-west-2.amazonaws.com`
- **Official documentation:** [Invite Team Member](https://help.ricoh360.com/hc/en-us/articles/360050751253-Team-Overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address of the invited team member. |
| `memberRole` | query | `string` | yes | Team member role enum, for example LIMITED or AGENT. Accepted values: `0`, `1`, `2`, `3`. |
| `teamId` | query | `string` | yes | Team ID to invite the member into. |
