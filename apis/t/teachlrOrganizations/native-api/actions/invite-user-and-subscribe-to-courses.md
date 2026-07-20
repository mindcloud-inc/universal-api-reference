# Invite User And Subscribe To Courses with Teachlr Organizations

## Endpoint

- **Method:** `POST`
- **Path:** `/invitations`
- **Base URL:** `https://api.teachlr.com/mindcloudteachlr337933/api`
- **Official documentation:** [Invite User And Subscribe To Courses](https://soporte.teachlr.com/base-de-conocimientos/como-invitar-un-usuario-a-una-escuela-y-opcionalmente-suscribirlo-a-uno-o-varios-cursos-usando-el-api-de-teachlr-organizaciones/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the user to invite. |
| `courses[]` | body | `array<number>` | yes | List of active Teachlr course IDs to subscribe the invited user to. |
