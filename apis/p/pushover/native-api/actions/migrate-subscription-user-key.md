# Migrate Subscription User Key with Pushover

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriptions/migrate.json`
- **Base URL:** `https://api.pushover.net/1`
- **Official documentation:** [Migrate Subscription User Key](https://pushover.net/api/subscriptions#migration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription` | query | `string` | yes | Subscription code identifying which subscription to migrate into. |
| `user` | query | `string` | yes | Existing Pushover user key to migrate. |
| `device_name` | query | `string` | no | Optional device name to limit the resulting subscription to one device. |
| `sound` | query | `string` | no | Optional preferred default sound to store with the subscription. |
