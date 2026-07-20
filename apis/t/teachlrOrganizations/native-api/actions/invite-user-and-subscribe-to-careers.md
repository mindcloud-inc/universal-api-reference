# Invite User And Subscribe To Careers with Teachlr Organizations

## Endpoint

- **Method:** `POST`
- **Path:** `/invitations`
- **Base URL:** `https://api.teachlr.com/mindcloudteachlr337933/api`
- **Official documentation:** [Invite User And Subscribe To Careers](https://soporte.teachlr.com/base-de-conocimientos/como-invitar-un-usuario-a-una-escuela-y-opcionalmente-suscribirlo-a-uno-o-varios-cursos-usando-el-api-de-teachlr-organizaciones/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the user to invite. |
| `careers[]` | body | `array<number>` | yes | List of Teachlr career IDs to subscribe the invited user to. |
