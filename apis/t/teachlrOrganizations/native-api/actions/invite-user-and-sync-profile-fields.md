# Invite User And Sync Profile Fields with Teachlr Organizations

## Endpoint

- **Method:** `POST`
- **Path:** `/invitations`
- **Base URL:** `https://api.teachlr.com/mindcloudteachlr337933/api`
- **Official documentation:** [Invite User And Sync Profile Fields](https://soporte.teachlr.com/base-de-conocimientos/como-invitar-un-usuario-a-una-escuela-y-opcionalmente-suscribirlo-a-uno-o-varios-cursos-usando-el-api-de-teachlr-organizaciones/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the user to invite or update. |
| `user_data` | body | `object` | no | Teachlr user profile fields to associate with the invited user, including optional update behavior. |
