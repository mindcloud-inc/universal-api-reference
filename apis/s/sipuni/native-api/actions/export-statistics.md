# Export Statistics with Sipuni

Exports filtered call statistics from Sipuni.

## Endpoint

- **Method:** `GET`
- **Path:** `/statistic/export`
- **Base URL:** `https://sipuni.com/api`
- **Official documentation:** [Export Statistics](https://doc.sipuni.com/articles/636-642--poluchenie-statistiki/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | Start date in DD.MM.YYYY format. |
| `to` | query | `string` | yes | End date in DD.MM.YYYY format. |
| `timeFrom` | query | `string` | no | — |
| `timeTo` | query | `string` | no | — |
| `type` | query | `string` | no | 0 all calls, 1 incoming, 2 outgoing, 3 internal. |
| `state` | query | `string` | no | 0 all calls, 1 missed, 2 answered. |
| `tree` | query | `string` | no | — |
| `showTreeId` | query | `string` | no | — |
| `fromNumber` | query | `string` | no | — |
| `toNumber` | query | `string` | no | — |
| `numbersRinged` | query | `string` | no | — |
| `numbersInvolved` | query | `string` | no | — |
| `names` | query | `string` | no | — |
| `outgoingLine` | query | `string` | no | — |
| `toAnswer` | query | `string` | no | — |
| `anonymous` | query | `string` | no | — |
| `firstTime` | query | `string` | no | — |
| `dtmfUserAnswer` | query | `string` | no | — |
