# Get Queue Statistics with Moderation API

Retrieves review queue statistics from Moderation API.

## Endpoint

- **Method:** `GET`
- **Path:** `/queue/:id/stats`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Get Queue Statistics](https://docs.moderationapi.com/api-reference/review-queues/get-queue-statistics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The queue ID |
| `withinDays` | query | `string` | no | Number of days to analyze statistics for |
