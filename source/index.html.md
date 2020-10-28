---
title: MeetWell API
language_tabs:
  - json: JSON
  - shell: cURL
---


# Action Items

Action or Parking Lot Items

## Create action item


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/185/action_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNzBlMzkzZS00NGY1LTQ2ZWUtYTM4My1lZDUyZmE2ZTMzMjAiLCJzdWIiOiI3NDgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTcsImV4cCI6MTYwNjA2NzExN30.L5BDdrMgFE561bjpEHxsVeuPPTSmyrRrR8mIjVKXAtY
```

`POST /api/v1/meetings/:meeting_id/action_items`

#### Parameters


```json
{"data":{"type":"action_item","attributes":{"description":"Discuss reticulating the splines.","owner_id":748,"creator_id":748,"category":"action_item","position":3,"due_by":"2020-10-29T17:45:17.531Z"}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| creator_id  | User id of person who created or suggested item |
| due_by  | Due date for addressing item |
| category  | Options: parking_lot or action_item (default) |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "24",
    "type": "action_items",
    "attributes": {
      "id": 24,
      "category": "action_item",
      "owner_name": "Illustrious Ultron Knight The Mimic",
      "owner_id": 748,
      "description": "Discuss reticulating the splines.",
      "creator_id": 748,
      "due_by": "2020-10-29T17:45:17.531Z",
      "position": 3,
      "creator_name": "Illustrious Ultron Knight The Mimic"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/185/action_items" -d '{"data":{"type":"action_item","attributes":{"description":"Discuss reticulating the splines.","owner_id":748,"creator_id":748,"category":"action_item","position":3,"due_by":"2020-10-29T17:45:17.531Z"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNzBlMzkzZS00NGY1LTQ2ZWUtYTM4My1lZDUyZmE2ZTMzMjAiLCJzdWIiOiI3NDgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTcsImV4cCI6MTYwNjA2NzExN30.L5BDdrMgFE561bjpEHxsVeuPPTSmyrRrR8mIjVKXAtY"
```
## Delete action item


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/182/action_items/22
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxNjhjZjRjYS1hOTFiLTQ2ZmEtOWQ1Yi05YzlmZTQ1NGI5MTIiLCJzdWIiOiI3NDEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTYsImV4cCI6MTYwNjA2NzExNn0.m6B3UtDZ6oNBnPJ634Z5uXbJ8gPxJQ5Ipql5VZTyqcU
```

`DELETE /api/v1/meetings/:meeting_id/action_items/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| creator_id  | User id of person who created or suggested item |
| due_by  | Due date for addressing item |
| category  | Options: parking_lot or action_item (default) |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/meetings/182/action_items/22" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxNjhjZjRjYS1hOTFiLTQ2ZmEtOWQ1Yi05YzlmZTQ1NGI5MTIiLCJzdWIiOiI3NDEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTYsImV4cCI6MTYwNjA2NzExNn0.m6B3UtDZ6oNBnPJ634Z5uXbJ8gPxJQ5Ipql5VZTyqcU"
```
## List action items


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/184/action_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmYjEwMWRlOS05MGQ3LTQ1YmQtOThmNC1mOWFiM2Q0ZTJmNmUiLCJzdWIiOiI3NDciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTcsImV4cCI6MTYwNjA2NzExN30.jyg_ns07x0Rs8MRhPCs_K6c_h-HYiu7cZu1TJM-M7ec
```

`GET /api/v1/meetings/:meeting_id/action_items`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| creator_id  | User id of person who created or suggested item |
| due_by  | Due date for addressing item |
| category  | Options: parking_lot or action_item (default) |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/184/action_items" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmYjEwMWRlOS05MGQ3LTQ1YmQtOThmNC1mOWFiM2Q0ZTJmNmUiLCJzdWIiOiI3NDciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTcsImV4cCI6MTYwNjA2NzExN30.jyg_ns07x0Rs8MRhPCs_K6c_h-HYiu7cZu1TJM-M7ec"
```
## Show action item


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/181/action_items/21
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjZGJlOTVkNi00MGIzLTRhY2UtOGFmOS0xNWE2ZTJiN2NiN2QiLCJzdWIiOiI3MzgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTYsImV4cCI6MTYwNjA2NzExNn0.oGVuk8rl3UaFbm4uMjnHiOwp98YiKaH-18Pz64Cr1sU
```

`GET /api/v1/meetings/:meeting_id/action_items/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| creator_id  | User id of person who created or suggested item |
| due_by  | Due date for addressing item |
| category  | Options: parking_lot or action_item (default) |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "21",
    "type": "action_items",
    "attributes": {
      "id": 21,
      "category": "action_item",
      "owner_name": "Multiple Green Nina Theroux Dragon",
      "owner_id": 739,
      "description": "Heirloom tacos direct trade single-origin coffee wolf selvage.",
      "creator_id": 740,
      "due_by": "2020-10-30T17:45:16.561Z",
      "position": null,
      "creator_name": "Trickster General Doc Samson"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/181/action_items/21" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjZGJlOTVkNi00MGIzLTRhY2UtOGFmOS0xNWE2ZTJiN2NiN2QiLCJzdWIiOiI3MzgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTYsImV4cCI6MTYwNjA2NzExNn0.oGVuk8rl3UaFbm4uMjnHiOwp98YiKaH-18Pz64Cr1sU"
```
## Update action item


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/183/action_items/23
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmNGNlNWU4YS03MDNhLTRiM2ItOWU4ZS05OTgxMjM0YmFkMGEiLCJzdWIiOiI3NDQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTcsImV4cCI6MTYwNjA2NzExN30.LqZya5HF4HCBHz_v8zYiKoWaZMp6Qomv_kgoPUcOWBE
```

`PUT /api/v1/meetings/:meeting_id/action_items/:id`

#### Parameters


```json
{"data":{"type":"action_item","attributes":{"description":"Talk.","owner_id":744,"creator_id":744,"category":"action_item","position":2,"due_by":"2020-10-29T17:45:17.022Z"}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| creator_id  | User id of person who created or suggested item |
| due_by  | Due date for addressing item |
| category  | Options: parking_lot or action_item (default) |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "23",
    "type": "action_items",
    "attributes": {
      "id": 23,
      "category": "action_item",
      "owner_name": "Doctor Kool-Aid Man Giant Jubilee",
      "owner_id": 744,
      "description": "Talk.",
      "creator_id": 744,
      "due_by": "2020-10-29T17:45:17.022Z",
      "position": 2,
      "creator_name": "Doctor Kool-Aid Man Giant Jubilee"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/183/action_items/23" -d '{"data":{"type":"action_item","attributes":{"description":"Talk.","owner_id":744,"creator_id":744,"category":"action_item","position":2,"due_by":"2020-10-29T17:45:17.022Z"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmNGNlNWU4YS03MDNhLTRiM2ItOWU4ZS05OTgxMjM0YmFkMGEiLCJzdWIiOiI3NDQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTcsImV4cCI6MTYwNjA2NzExN30.LqZya5HF4HCBHz_v8zYiKoWaZMp6Qomv_kgoPUcOWBE"
```
# Actions



## List future actions


### Request

#### Endpoint

```plaintext
GET /api/v1/future_actions?by_period[starts_at]=2020-10-28+17%3A45%3A12+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A12+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkNGVhZTkxZS01M2EyLTQyNzQtYTc2NS0xMTFiMTM0OGQzOTQiLCJzdWIiOiI3MDkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.RLrg0X3euF5uGlwwCzcok4Xnw56QoxFprxUIMcBo_Fk
```

`GET /api/v1/future_actions`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:12 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:12 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/future_actions?by_period[starts_at]=2020-10-28+17%3A45%3A12+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A12+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkNGVhZTkxZS01M2EyLTQyNzQtYTc2NS0xMTFiMTM0OGQzOTQiLCJzdWIiOiI3MDkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.RLrg0X3euF5uGlwwCzcok4Xnw56QoxFprxUIMcBo_Fk"
```
## List past actions


### Request

#### Endpoint

```plaintext
GET /api/v1/past_actions?by_period[starts_at]=2020-10-28+17%3A45%3A24+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A24+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2YjMxY2UwYS1hZTg2LTQxMWMtYTQwYS02ZjUzYTFlNDA4NWMiLCJzdWIiOiI3OTEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjQsImV4cCI6MTYwNjA2NzEyNH0.biaZ4PGzM3_pDUIMjdq-nl4HRvJoctJM4HL4KT8UJ0c
```

`GET /api/v1/past_actions`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:24 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:24 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/past_actions?by_period[starts_at]=2020-10-28+17%3A45%3A24+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A24+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2YjMxY2UwYS1hZTg2LTQxMWMtYTQwYS02ZjUzYTFlNDA4NWMiLCJzdWIiOiI3OTEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjQsImV4cCI6MTYwNjA2NzEyNH0.biaZ4PGzM3_pDUIMjdq-nl4HRvJoctJM4HL4KT8UJ0c"
```
# Agenda Items



## Create agenda item


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/199/agenda_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxZGUxMDkwYy0xMGYwLTRkNmItYTU1Ny1jNzBkMGU1OTQ5MTMiLCJzdWIiOiI3ODUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjMsImV4cCI6MTYwNjA2NzEyM30.de6HFnXtdpcuZAaNMc4VOMMPiQyClG9tHiNHto1tS8E
```

`POST /api/v1/meetings/:meeting_id/agenda_items`

#### Parameters


```json
{"data":{"type":"agenda_item","attributes":{"description":"Discuss reticulating the splines.","owner_id":785,"position":3,"duration_in_mins":15,"started_at":"2020-10-28T17:43:23.113Z"}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| started_at  | The datestamp for when the agenda discussion began |
| duration_in_mins  | Timebox for agenda item |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "23",
    "type": "agenda_items",
    "attributes": {
      "id": 23,
      "owner_name": "Buffy III Doctor Banshee",
      "owner_id": 785,
      "description": "Discuss reticulating the splines.",
      "duration_in_mins": 15,
      "time_spent_in_secs": null,
      "started_at": "2020-10-28T17:43:23.113Z",
      "ended_at": null,
      "meeting_id": 199,
      "position": 3
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/199/agenda_items" -d '{"data":{"type":"agenda_item","attributes":{"description":"Discuss reticulating the splines.","owner_id":785,"position":3,"duration_in_mins":15,"started_at":"2020-10-28T17:43:23.113Z"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxZGUxMDkwYy0xMGYwLTRkNmItYTU1Ny1jNzBkMGU1OTQ5MTMiLCJzdWIiOiI3ODUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjMsImV4cCI6MTYwNjA2NzEyM30.de6HFnXtdpcuZAaNMc4VOMMPiQyClG9tHiNHto1tS8E"
```
## Delete agenda item


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/200/agenda_items/24
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwMjdiMzVlMi01NzFkLTQyOTItOGE5YS1kMDU1NzNkMjkxMzMiLCJzdWIiOiI3ODYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjMsImV4cCI6MTYwNjA2NzEyM30.gJZjtE3pzCJcSPEmlmS30q6KEcoOVIGCEVvlg707V-8
```

`DELETE /api/v1/meetings/:meeting_id/agenda_items/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| started_at  | The datestamp for when the agenda discussion began |
| duration_in_mins  | Timebox for agenda item |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/meetings/200/agenda_items/24" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwMjdiMzVlMi01NzFkLTQyOTItOGE5YS1kMDU1NzNkMjkxMzMiLCJzdWIiOiI3ODYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjMsImV4cCI6MTYwNjA2NzEyM30.gJZjtE3pzCJcSPEmlmS30q6KEcoOVIGCEVvlg707V-8"
```
## List agenda items


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/198/agenda_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMTRmMzIwZi0yMGY3LTQwNzktYTY2NC0xMjg1NDZjNWVhNzEiLCJzdWIiOiI3ODQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjIsImV4cCI6MTYwNjA2NzEyMn0.HAdF8iT6bdyPNjazxyGKIgCgZx4NBFjBsQbcLJvhutM
```

`GET /api/v1/meetings/:meeting_id/agenda_items`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| started_at  | The datestamp for when the agenda discussion began |
| duration_in_mins  | Timebox for agenda item |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/198/agenda_items" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMTRmMzIwZi0yMGY3LTQwNzktYTY2NC0xMjg1NDZjNWVhNzEiLCJzdWIiOiI3ODQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjIsImV4cCI6MTYwNjA2NzEyMn0.HAdF8iT6bdyPNjazxyGKIgCgZx4NBFjBsQbcLJvhutM"
```
## Show agenda item


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/196/agenda_items/21
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4Yjk2YzUzMC1jNjg5LTQ5NDEtOTk1Mi1hMzZiNDUzMjU5YzAiLCJzdWIiOiI3ODAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjIsImV4cCI6MTYwNjA2NzEyMn0.XPkEx_7xBOPFY63BRlC9SvTLUT9UYXQhgZzNmmZcllI
```

`GET /api/v1/meetings/:meeting_id/agenda_items/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| started_at  | The datestamp for when the agenda discussion began |
| duration_in_mins  | Timebox for agenda item |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "21",
    "type": "agenda_items",
    "attributes": {
      "id": 21,
      "owner_name": "Nina Theroux Gladiator",
      "owner_id": 781,
      "description": "Viral semiotics pbr&b.",
      "duration_in_mins": 70,
      "time_spent_in_secs": null,
      "started_at": null,
      "ended_at": null,
      "meeting_id": 196,
      "position": 2
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/196/agenda_items/21" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4Yjk2YzUzMC1jNjg5LTQ5NDEtOTk1Mi1hMzZiNDUzMjU5YzAiLCJzdWIiOiI3ODAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjIsImV4cCI6MTYwNjA2NzEyMn0.XPkEx_7xBOPFY63BRlC9SvTLUT9UYXQhgZzNmmZcllI"
```
## Update agenda item


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/197/agenda_items/22
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5Nzg2ODc1My04ZjFhLTRjZTMtOTYyZC04MjZjYjY1ZWVlOWEiLCJzdWIiOiI3ODIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjIsImV4cCI6MTYwNjA2NzEyMn0.Qh-8Mm2tMt3QG3ct3FCk8nBhlZcPlMXrWx3AztTIHII
```

`PUT /api/v1/meetings/:meeting_id/agenda_items/:id`

#### Parameters


```json
{"data":{"type":"agenda_item","attributes":{"description":"Talk about things"}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |
| owner_id  | User id of person responsible for item |
| started_at  | The datestamp for when the agenda discussion began |
| duration_in_mins  | Timebox for agenda item |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "22",
    "type": "agenda_items",
    "attributes": {
      "id": 22,
      "owner_name": "Giant Luna Spirit Bomb Queen",
      "owner_id": 783,
      "description": "Talk about things",
      "duration_in_mins": 73,
      "time_spent_in_secs": null,
      "started_at": null,
      "ended_at": null,
      "meeting_id": 197,
      "position": 2
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/197/agenda_items/22" -d '{"data":{"type":"agenda_item","attributes":{"description":"Talk about things"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5Nzg2ODc1My04ZjFhLTRjZTMtOTYyZC04MjZjYjY1ZWVlOWEiLCJzdWIiOiI3ODIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjIsImV4cCI6MTYwNjA2NzEyMn0.Qh-8Mm2tMt3QG3ct3FCk8nBhlZcPlMXrWx3AztTIHII"
```
# Articles



## Create article


### Request

#### Endpoint

```plaintext
POST /api/v1/articles
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4N2JhMjMzZS1kMzUyLTQ4YmEtOTkwMy04M2Y2NzdkOTFjM2UiLCJzdWIiOiI3MTkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTMsImV4cCI6MTYwNjA2NzExM30.RV1Y8aviC-ULO4DFDwD6iOhmiz6Om3HzLj0CXZz8ZkM
```

`POST /api/v1/articles`

#### Parameters


```json
{"data":{"type":"article","attributes":{"title":"Testing","url":"http://www.meetwell.app","tag_list":"tesing,fun"}}}
```


| Name | Description |
|:-----|:------------|
| tagged_with  | List articles tagged with value |
| not_tagged_with  | List articles not tagged with value |
| order  | Order by column or random |
| title *required* |  title |
| tag_list *required* |  tag list |
| url  |  url |
| pull_quote  |  pull quote |
| publish_on  |  publish on |
| position  |  position |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "27",
    "type": "articles",
    "attributes": {
      "id": 27,
      "title": "Testing",
      "url": "http://www.meetwell.app",
      "pull_quote": null,
      "description": null,
      "position": null,
      "publish_on": "2020-10-28T17:45:13.539Z",
      "tag_list": [
        "tesing",
        "fun"
      ]
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/articles" -d '{"data":{"type":"article","attributes":{"title":"Testing","url":"http://www.meetwell.app","tag_list":"tesing,fun"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4N2JhMjMzZS1kMzUyLTQ4YmEtOTkwMy04M2Y2NzdkOTFjM2UiLCJzdWIiOiI3MTkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTMsImV4cCI6MTYwNjA2NzExM30.RV1Y8aviC-ULO4DFDwD6iOhmiz6Om3HzLj0CXZz8ZkM"
```
## Delete article


### Request

#### Endpoint

```plaintext
DELETE /api/v1/articles/25
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmM2VjYmQ2Yy0yMTNiLTQ4MzEtOGNmMS1lM2M0NjZmNTAzYTgiLCJzdWIiOiI3MTciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTMsImV4cCI6MTYwNjA2NzExM30.ZNfR4v0QOQbN6RjmKKVnb_OhlTx3shh0qW2nw-H3-NE
```

`DELETE /api/v1/articles/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| tagged_with  | List articles tagged with value |
| not_tagged_with  | List articles not tagged with value |
| order  | Order by column or random |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/articles/25" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmM2VjYmQ2Yy0yMTNiLTQ4MzEtOGNmMS1lM2M0NjZmNTAzYTgiLCJzdWIiOiI3MTciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTMsImV4cCI6MTYwNjA2NzExM30.ZNfR4v0QOQbN6RjmKKVnb_OhlTx3shh0qW2nw-H3-NE"
```
## List articles


### Request

#### Endpoint

```plaintext
GET /api/v1/articles
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3NzkyMmEyZS01YjIzLTQyOTMtOTg0NC1iMDZmM2I4M2RmZWYiLCJzdWIiOiI3MTYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTMsImV4cCI6MTYwNjA2NzExM30.bqa_-yPZ9-ANRD8v-RRKYHWhWOIHjnJOOW34kgge-gU
```

`GET /api/v1/articles`

#### Parameters



| Name | Description |
|:-----|:------------|
| tagged_with  | List articles tagged with value |
| not_tagged_with  | List articles not tagged with value |
| order  | Order by column or random |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "1",
      "type": "articles",
      "attributes": {
        "id": 1,
        "title": "Maker's Schedule, Manager's Schedule",
        "url": "http://www.paulgraham.com/makersschedule.html",
        "pull_quote": "When you're operating on the maker's schedule, meetings are a disaster. A single meeting can blow a whole afternoon, by breaking it into two pieces each too small to do anything hard in. --Paul Graham",
        "description": null,
        "position": null,
        "publish_on": "2020-10-28T17:21:49.033Z",
        "tag_list": [
          "defend",
          "focus-block",
          "paul-graham",
          "makers-schedule"
        ]
      }
    },
    {
      "id": "2",
      "type": "articles",
      "attributes": {
        "id": 2,
        "title": "Why work doesn't happen at work",
        "url": "https://www.ted.com/talks/jason_fried_why_work_doesn_t_happen_at_work",
        "pull_quote": "At the office, most of the interruptions and distractions that really cause people not to get work done are involuntary. ...[Managers and meetings]  keep interrupting you at the wrong time, while you're actually trying to do something they're paying you to do, they tend to interrupt you. That's kind of bad. --Jason Fried",
        "description": null,
        "position": null,
        "publish_on": "2020-10-28T17:21:49.071Z",
        "tag_list": [
          "defend",
          "focus-block",
          "jason-fried"
        ]
      }
    },
    {
      "id": "3",
      "type": "articles",
      "attributes": {
        "id": 3,
        "title": "Studies show the ideal number of people for a meeting is less than 8.",
        "url": "https://www.forbes.com/sites/victoriafine/2018/04/16/why-you-should-never-invite-more-than-7-people-to-your-meeting/#667f1fcd434c",
        "pull_quote": "You shouldn’t invite more than seven people in a meeting, ever. --Victoria Fine",
        "description": null,
        "position": null,
        "publish_on": "2020-10-28T17:21:49.083Z",
        "tag_list": [
          "max-attendees",
          "victoria-fine"
        ]
      }
    },
    {
      "id": "4",
      "type": "articles",
      "attributes": {
        "id": 4,
        "title": "You can say No: 3 ways to turn down a last-minute meeting request",
        "url": "https://www.themuse.com/advice/you-can-say-no-3-ways-to-turn-down-a-lastminute-meeting-request",
        "pull_quote": "It’s possible to say no to a last-minute meeting and still look like a team player. --Sara McCord",
        "description": null,
        "position": null,
        "publish_on": "2020-10-28T17:21:49.096Z",
        "tag_list": [
          "last-minute",
          "sara-mccord"
        ]
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/articles" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3NzkyMmEyZS01YjIzLTQyOTMtOTg0NC1iMDZmM2I4M2RmZWYiLCJzdWIiOiI3MTYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTMsImV4cCI6MTYwNjA2NzExM30.bqa_-yPZ9-ANRD8v-RRKYHWhWOIHjnJOOW34kgge-gU"
```
## Show article


### Request

#### Endpoint

```plaintext
GET /api/v1/articles/28
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwNzNhNTZkMS02NjhiLTQ1ZjItYWVjOC01YzQ4YmZlMDVmNDkiLCJzdWIiOiI3MjAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTMsImV4cCI6MTYwNjA2NzExM30.HAqpkTe9FnJXhPM9ZNc06-dFxrV3m-I_lzIVVOShpUo
```

`GET /api/v1/articles/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| tagged_with  | List articles tagged with value |
| not_tagged_with  | List articles not tagged with value |
| order  | Order by column or random |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "28",
    "type": "articles",
    "attributes": {
      "id": 28,
      "title": "3 wolf moon yuccie next level letterpress green juice truffaut.",
      "url": "http://smith-nader.net/carol_rolfson",
      "pull_quote": "Stumptown poutine raw denim locavore chartreuse fanny pack vegan kombucha heirloom jean shorts roof readymade.",
      "description": null,
      "position": null,
      "publish_on": "2020-10-28T17:45:13.646Z",
      "tag_list": [
        "tool-tip",
        "test"
      ]
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/articles/28" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwNzNhNTZkMS02NjhiLTQ1ZjItYWVjOC01YzQ4YmZlMDVmNDkiLCJzdWIiOiI3MjAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTMsImV4cCI6MTYwNjA2NzExM30.HAqpkTe9FnJXhPM9ZNc06-dFxrV3m-I_lzIVVOShpUo"
```
## Update article


### Request

#### Endpoint

```plaintext
PUT /api/v1/articles/26
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlMDc0ZDg5NC01MzFiLTQ4NzgtOTI5MC03OTdjMmM2NGQxZGEiLCJzdWIiOiI3MTgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTMsImV4cCI6MTYwNjA2NzExM30.0WWyWCd45c4e8LaXykkt9ISI7BlMAHjmvXFTs3FZuX8
```

`PUT /api/v1/articles/:id`

#### Parameters


```json
{"data":{"type":"article","attributes":{"title":"Testing again"}}}
```


| Name | Description |
|:-----|:------------|
| tagged_with  | List articles tagged with value |
| not_tagged_with  | List articles not tagged with value |
| order  | Order by column or random |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "26",
    "type": "articles",
    "attributes": {
      "id": 26,
      "title": "Testing again",
      "url": "http://frami.io/magdalena_damore",
      "pull_quote": "Blue bottle tousled cleanse synth austin twee swag venmo fashion axe tote bag marfa you probably haven't heard of them goth.",
      "description": null,
      "position": null,
      "publish_on": "2020-10-28T17:45:13.410Z",
      "tag_list": [
        "tool-tip",
        "test"
      ]
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/articles/26" -d '{"data":{"type":"article","attributes":{"title":"Testing again"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlMDc0ZDg5NC01MzFiLTQ4NzgtOTI5MC03OTdjMmM2NGQxZGEiLCJzdWIiOiI3MTgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTMsImV4cCI6MTYwNjA2NzExM30.0WWyWCd45c4e8LaXykkt9ISI7BlMAHjmvXFTs3FZuX8"
```
# Attendees



## Create attendee


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/188/attendees
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmMmNjMmIwZi0yODNmLTRlMmYtYTdhNi1jZmE0MzUwNTczNGMiLCJzdWIiOiI3NjUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTksImV4cCI6MTYwNjA2NzExOX0.9-joxWhomla_n49On1joOBKBQu7Ohg6ZWqRAKhiZ97Q
```

`POST /api/v1/meetings/:meeting_id/attendees`

#### Parameters


```json
{"data":{"type":"attendee","attributes":{"email":"test@test.com","attendee_name":"Test","status":"confirmed"}}}
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |
| status_ *required* | Actual key is status |
| user_id  |  user |
| attendee_name  |  attendee name |
| role  | organizer, note_taker, subject_matter_expert, stakeholder, decision_maker |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "97",
    "type": "attendees",
    "attributes": {
      "id": 97,
      "email": "test@test.com",
      "status": "confirmed",
      "role": null,
      "attendee_name": null
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/188/attendees" -d '{"data":{"type":"attendee","attributes":{"email":"test@test.com","attendee_name":"Test","status":"confirmed"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmMmNjMmIwZi0yODNmLTRlMmYtYTdhNi1jZmE0MzUwNTczNGMiLCJzdWIiOiI3NjUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTksImV4cCI6MTYwNjA2NzExOX0.9-joxWhomla_n49On1joOBKBQu7Ohg6ZWqRAKhiZ97Q"
```
## Delete agenda item


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/186/attendees/96
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlOGZmYWM4Ny1hODNhLTQ1MDItYWMwMy1jZTkzMTY4MWZlNmMiLCJzdWIiOiI3NjIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTksImV4cCI6MTYwNjA2NzExOX0.LgbWpo4mcRergsC1hdiiaZ7dVXTc3KrZmKQlZ_oIUJo
```

`DELETE /api/v1/meetings/:meeting_id/attendees/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| email *required* |  email |
| status_ *required* | Actual key is status |
| user_id  |  user |
| attendee_name  |  attendee name |
| role  | organizer, note_taker, subject_matter_expert, stakeholder, decision_maker |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/meetings/186/attendees/96" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlOGZmYWM4Ny1hODNhLTQ1MDItYWMwMy1jZTkzMTY4MWZlNmMiLCJzdWIiOiI3NjIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTksImV4cCI6MTYwNjA2NzExOX0.LgbWpo4mcRergsC1hdiiaZ7dVXTc3KrZmKQlZ_oIUJo"
```
## List attendees


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/187/attendees
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiY2Y3ZTBmYy1jY2NmLTQ2NzEtYjYxMi1mNTc1YjAwOGI4MjciLCJzdWIiOiI3NjQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTksImV4cCI6MTYwNjA2NzExOX0.V6q9qEoXtsjtfJFtsro969M9018G_6oIRC4GcLYTkjY
```

`GET /api/v1/meetings/:meeting_id/attendees`

#### Parameters



| Name | Description |
|:-----|:------------|
| email *required* |  email |
| status_ *required* | Actual key is status |
| user_id  |  user |
| attendee_name  |  attendee name |
| role  | organizer, note_taker, subject_matter_expert, stakeholder, decision_maker |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/187/attendees" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiY2Y3ZTBmYy1jY2NmLTQ2NzEtYjYxMi1mNTc1YjAwOGI4MjciLCJzdWIiOiI3NjQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTksImV4cCI6MTYwNjA2NzExOX0.V6q9qEoXtsjtfJFtsro969M9018G_6oIRC4GcLYTkjY"
```
## Show attendee


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/189/attendees/98
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNjFhYTQ0Mi0xYTQyLTQxY2MtYjA0ZS1kZjUxNTBhMDdiZWMiLCJzdWIiOiI3NjYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjAsImV4cCI6MTYwNjA2NzEyMH0.IUCGmxGCLCgESfZdoRDfv-2RevvT5YWkGVaeo8XfmSY
```

`GET /api/v1/meetings/:meeting_id/attendees/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| email *required* |  email |
| status_ *required* | Actual key is status |
| user_id  |  user |
| attendee_name  |  attendee name |
| role  | organizer, note_taker, subject_matter_expert, stakeholder, decision_maker |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "98",
    "type": "attendees",
    "attributes": {
      "id": 98,
      "email": "lorraine.fritsch@mosciski-hilpert.info",
      "status": "confirmed",
      "role": "subject_matter_expert",
      "attendee_name": null
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/189/attendees/98" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNjFhYTQ0Mi0xYTQyLTQxY2MtYjA0ZS1kZjUxNTBhMDdiZWMiLCJzdWIiOiI3NjYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjAsImV4cCI6MTYwNjA2NzEyMH0.IUCGmxGCLCgESfZdoRDfv-2RevvT5YWkGVaeo8XfmSY"
```
## Update attendee


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/190/attendees/99
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0M2MyNjQwMC1mZmFmLTQxMDgtODk5ZS0zMjI2ZjI2NTVjNzgiLCJzdWIiOiI3NjgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjAsImV4cCI6MTYwNjA2NzEyMH0.e1QNAPKmfNtDtdSC4baDxDY6W3lFv-HzB2b5CQUtSiE
```

`PUT /api/v1/meetings/:meeting_id/attendees/:id`

#### Parameters


```json
{"data":{"type":"attendee","attributes":{"attendee_name":"Test 2"}}}
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |
| status_ *required* | Actual key is status |
| user_id  |  user |
| attendee_name  |  attendee name |
| role  | organizer, note_taker, subject_matter_expert, stakeholder, decision_maker |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "99",
    "type": "attendees",
    "attributes": {
      "id": 99,
      "email": "erik.cormier@nicolas-corkery.co",
      "status": "confirmed",
      "role": "subject_matter_expert",
      "attendee_name": null
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/190/attendees/99" -d '{"data":{"type":"attendee","attributes":{"attendee_name":"Test 2"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0M2MyNjQwMC1mZmFmLTQxMDgtODk5ZS0zMjI2ZjI2NTVjNzgiLCJzdWIiOiI3NjgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjAsImV4cCI6MTYwNjA2NzEyMH0.e1QNAPKmfNtDtdSC4baDxDY6W3lFv-HzB2b5CQUtSiE"
```
# Calendars



## List added calendars


### Request

#### Endpoint

```plaintext
GET /api/v1/calendars
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2ZjM5OTRkMC01YWUzLTQ4NzctYmQzZi00MzRlOWYyNzc3ZjkiLCJzdWIiOiI3MjgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.J2w986S-cT-6sh3uiPKolAgogr-YLJ5-H3vNGzSAN_Q
```

`GET /api/v1/calendars`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "755",
      "type": "calendars",
      "attributes": {
        "name": "Stacy X Dragon",
        "primary": false,
        "source": "google",
        "uuid": "e17213da-014d-4ac1-b180-ac85f000f511",
        "watching": false
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/calendars" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2ZjM5OTRkMC01YWUzLTQ4NzctYmQzZi00MzRlOWYyNzc3ZjkiLCJzdWIiOiI3MjgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.J2w986S-cT-6sh3uiPKolAgogr-YLJ5-H3vNGzSAN_Q"
```
# Communication Preferences

Opt-in/out of email communications for non-registered users

## Email Opt In


### Request

#### Endpoint

```plaintext
GET /api/v1/communications/email/opt-in?email=test%40test.com
Content-Type: application/vnd.api+json
```

`GET /api/v1/communications/email/opt-in`

#### Parameters


```json
email: test@test.com
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext
Content-Type: text/plain; charset=utf-8
201 Created
```


```json
 
```



```shell
curl -g "http://localhost:3000/api/v1/communications/email/opt-in?email=test%40test.com" -X GET \
	-H "Content-Type: application/vnd.api+json"
```
## Email Opt Out


### Request

#### Endpoint

```plaintext
GET /api/v1/communications/email/opt-out?email=test%40test.com
Content-Type: application/vnd.api+json
```

`GET /api/v1/communications/email/opt-out`

#### Parameters


```json
email: test@test.com
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext

204 No Content
```




```shell
curl -g "http://localhost:3000/api/v1/communications/email/opt-out?email=test%40test.com" -X GET \
	-H "Content-Type: application/vnd.api+json"
```
## Non-registered email is not opted-out


### Request

#### Endpoint

```plaintext
GET /api/v1/communications/email/opted-out?email=test%40test.com
Content-Type: application/vnd.api+json
```

`GET /api/v1/communications/email/opted-out`

#### Parameters


```json
email: test@test.com
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext
Content-Type: text/plain; charset=utf-8
200 OK
```


```json
 
```



```shell
curl -g "http://localhost:3000/api/v1/communications/email/opted-out?email=test%40test.com" -X GET \
	-H "Content-Type: application/vnd.api+json"
```
## Non-registered email is opted-out


### Request

#### Endpoint

```plaintext
GET /api/v1/communications/email/opted-out?email=test%40test.com
Content-Type: application/vnd.api+json
```

`GET /api/v1/communications/email/opted-out`

#### Parameters


```json
email: test@test.com
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext

204 No Content
```




```shell
curl -g "http://localhost:3000/api/v1/communications/email/opted-out?email=test%40test.com" -X GET \
	-H "Content-Type: application/vnd.api+json"
```
## User is registered in system


### Request

#### Endpoint

```plaintext
GET /api/v1/communications/email/opted-out?email=test%40test.com
Content-Type: application/vnd.api+json
```

`GET /api/v1/communications/email/opted-out`

#### Parameters


```json
email: test@test.com
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext

304 Not Modified
```




```shell
curl -g "http://localhost:3000/api/v1/communications/email/opted-out?email=test%40test.com" -X GET \
	-H "Content-Type: application/vnd.api+json"
```
# Goals



## List goals


### Request

#### Endpoint

```plaintext
GET /api/v1/goals
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1ODc1NTQ1MC0zMWFlLTQxOTEtYjFjNS05NGI2OTc3OWQ1YmYiLCJzdWIiOiI3MzciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTYsImV4cCI6MTYwNjA2NzExNn0.BnCElPgtHx9e3wJ7AWkZisJejxUCUo46N1rIDnYp3HU
```

`GET /api/v1/goals`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "11",
      "type": "goals",
      "attributes": {
        "key": "backpack",
        "name": "🎒 Go backpacking",
        "position": null
      }
    },
    {
      "id": "1",
      "type": "goals",
      "attributes": {
        "key": "be_creative",
        "name": "🎨 Be creative",
        "position": null
      }
    },
    {
      "id": "6",
      "type": "goals",
      "attributes": {
        "key": "be_strategic",
        "name": "📆 Be more strategic",
        "position": null
      }
    },
    {
      "id": "8",
      "type": "goals",
      "attributes": {
        "key": "exercise",
        "name": "💪 Exercise",
        "position": null
      }
    },
    {
      "id": "5",
      "type": "goals",
      "attributes": {
        "key": "get_things_done",
        "name": "🖋 Get things done",
        "position": null
      }
    },
    {
      "id": "3",
      "type": "goals",
      "attributes": {
        "key": "hang_with_kids",
        "name": "😎 Hang with the kids",
        "position": null
      }
    },
    {
      "id": "2",
      "type": "goals",
      "attributes": {
        "key": "learn_something",
        "name": "🏄 Learn something new",
        "position": null
      }
    },
    {
      "id": "9",
      "type": "goals",
      "attributes": {
        "key": "meditate",
        "name": "😌 Meditate",
        "position": null
      }
    },
    {
      "id": "10",
      "type": "goals",
      "attributes": {
        "key": "sleep",
        "name": "😪 Sleep",
        "position": null
      }
    },
    {
      "id": "12",
      "type": "goals",
      "attributes": {
        "key": "sports",
        "name": "⚾️ Watch sports",
        "position": null
      }
    },
    {
      "id": "7",
      "type": "goals",
      "attributes": {
        "key": "take_time_off",
        "name": "⏱ Take some time off",
        "position": null
      }
    },
    {
      "id": "4",
      "type": "goals",
      "attributes": {
        "key": "time_with_spouse",
        "name": "😘 Spend time with your partner",
        "position": null
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/goals" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1ODc1NTQ1MC0zMWFlLTQxOTEtYjFjNS05NGI2OTc3OWQ1YmYiLCJzdWIiOiI3MzciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTYsImV4cCI6MTYwNjA2NzExNn0.BnCElPgtHx9e3wJ7AWkZisJejxUCUo46N1rIDnYp3HU"
```
# Google Calendar



## List Google Calendars


### Request

#### Endpoint

```plaintext
GET /api/v1/google_calendar/list
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwNzU1ZGMzYS1jOTUxLTRhODItODIxNS02YTU0ZTIwMWM1NTAiLCJzdWIiOiI3MzUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.WTjAtroHWa1GGHqiSdnQQEjFAiA282kO2S25hk4bkDw
```

`GET /api/v1/google_calendar/list`

#### Parameters



| Name | Description |
|:-----|:------------|
| show_deleted  | Show deleted Google calendars |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "family08643361170578082544@group.calendar.google.com",
      "type": "external_calendars",
      "attributes": {
        "name": "Family",
        "primary": false,
        "deleted": null
      }
    },
    {
      "id": "6i5saadl27kpd8b7mgg2van2kt_20191030T200000Z",
      "type": "external_calendars",
      "attributes": {
        "name": "Personal",
        "primary": true,
        "deleted": null
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/google_calendar/list" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwNzU1ZGMzYS1jOTUxLTRhODItODIxNS02YTU0ZTIwMWM1NTAiLCJzdWIiOiI3MzUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.WTjAtroHWa1GGHqiSdnQQEjFAiA282kO2S25hk4bkDw"
```
## Setup Google Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/google_calendar/webhooks_setup
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzNzY1MWQzZS0yNTMyLTRmNmYtODU2NC03YTE0ODIzZmNlNmYiLCJzdWIiOiI3MTMiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.lGDrP_aMODgnXQnpf-_KmsorsyOIsD7Yft-d8nSowRU
```

`POST /api/v1/google_calendar/webhooks_setup`

#### Parameters


```json
{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| calendar_uuid *required* | Google Calendar UUID |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/google_calendar/webhooks_setup" -d '{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzNzY1MWQzZS0yNTMyLTRmNmYtODU2NC03YTE0ODIzZmNlNmYiLCJzdWIiOiI3MTMiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.lGDrP_aMODgnXQnpf-_KmsorsyOIsD7Yft-d8nSowRU"
```
## Stop Google Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/google_calendar/webhooks_stop
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5ODUwNDI4NS00MTNhLTRkMmMtODY3Ni00MmQ4ZjQxNmY1M2UiLCJzdWIiOiI3MTIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.X4d25C7vcu8RESQbX169qWRproBEIMek2AIWyDosWuE
```

`POST /api/v1/google_calendar/webhooks_stop`

#### Parameters


```json
{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| calendar_uuid *required* | Google Calendar UUID |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/google_calendar/webhooks_stop" -d '{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5ODUwNDI4NS00MTNhLTRkMmMtODY3Ni00MmQ4ZjQxNmY1M2UiLCJzdWIiOiI3MTIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.X4d25C7vcu8RESQbX169qWRproBEIMek2AIWyDosWuE"
```
## Watch Google Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/google_calendar/events/watch
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjOGNiMDE1MC0zYTUxLTRjMzYtODMxOC01ODlkMmQwZmNmYjEiLCJzdWIiOiI3MTQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.mVZuzutKkkJoGGJTaGfvjx9zFzUr5NwB-cvi_dn4Mrc
```

`POST /api/v1/google_calendar/events/watch`

#### Parameters


None known.


### Response

```plaintext
Content-Type: text/plain; charset=utf-8
200 OK
```


```json
 
```



```shell
curl "http://localhost:3000/api/v1/google_calendar/events/watch" -d '' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjOGNiMDE1MC0zYTUxLTRjMzYtODMxOC01ODlkMmQwZmNmYjEiLCJzdWIiOiI3MTQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.mVZuzutKkkJoGGJTaGfvjx9zFzUr5NwB-cvi_dn4Mrc" \
	-H "X-Goog-Channel: 0451a650-d138-4016-a432-cea9a13cec89" \
	-H "X-Goog-Resource: 7d20862b-d17d-4728-b8dd-b6aa84816297"
```
# Invoices



## Get invoices


### Request

#### Endpoint

```plaintext
GET /api/v1/invoices
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3N2UzYTVmZS1lYzljLTQ4OTUtYjAzMC1lYTRlNWIyZDkxZGEiLCJzdWIiOiI3MTAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.A89_boiWJF8S9DAdxz7EqlJmS7cc2NTovHkhYM8Znno
```

`GET /api/v1/invoices`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/invoices" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3N2UzYTVmZS1lYzljLTQ4OTUtYjAzMC1lYTRlNWIyZDkxZGEiLCJzdWIiOiI3MTAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.A89_boiWJF8S9DAdxz7EqlJmS7cc2NTovHkhYM8Znno"
```
# Meeting Categories



## List meeting categories


### Request

#### Endpoint

```plaintext
GET /api/v1/meeting_categories
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwODQyYmExYy02MDI0LTQ0YmQtYmY2NS04YTlmMWMwOGYwMTgiLCJzdWIiOiI3MzIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.U7QTNUOc-e8AHXsgGfwkRPlMzeeP0eE5huamrf18tt0
```

`GET /api/v1/meeting_categories`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "d2e474ed-0812-411d-8cf4-6bff859d4e1a",
    "type": "meeting_categories",
    "attributes": {
      "labels": {
        "recurring": "Recurring",
        "all_hands": "All hands",
        "one_on_one": "One on one",
        "all_day": "All day",
        "unassigned": "Unassigned"
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meeting_categories" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwODQyYmExYy02MDI0LTQ0YmQtYmY2NS04YTlmMWMwOGYwMTgiLCJzdWIiOiI3MzIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.U7QTNUOc-e8AHXsgGfwkRPlMzeeP0eE5huamrf18tt0"
```
# Meeting Intentions



## List meeting intentions


### Request

#### Endpoint

```plaintext
GET /api/v1/meeting_intentions
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxNzQzMTRmYy0wYjc3LTRjMDItYTE0Ny1iYTk5ZWE3N2NlZWIiLCJzdWIiOiI4MTMiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.G1na5L63WqH_Z8tjjZMktmRm-f_-Cl_APc8sVeWAkPg
```

`GET /api/v1/meeting_intentions`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "04a2b60e-996d-4df0-8c5f-013adcb5beae",
    "type": "meeting_intentions",
    "attributes": {
      "labels": {
        "standup": "Stand up",
        "planning": "Planning",
        "retrospective": "Retrospective",
        "information": "Info sharing",
        "brainstorming": "Brainstorming",
        "consensus": "Decision Making",
        "kickoff": "Kick-off",
        "teambuilding": "Team building",
        "unassigned": "Unassigned"
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meeting_intentions" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxNzQzMTRmYy0wYjc3LTRjMDItYTE0Ny1iYTk5ZWE3N2NlZWIiLCJzdWIiOiI4MTMiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.G1na5L63WqH_Z8tjjZMktmRm-f_-Cl_APc8sVeWAkPg"
```
# Meetings



## Accept a meeting invite


### Request

#### Endpoint

```plaintext
GET /api/v1/users/meetings/accept/203
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhY2U4OWZiYi03ODI2LTQ1OWUtYjUxOC1hODhiOWZmMGIyZGUiLCJzdWIiOiI3OTgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjUsImV4cCI6MTYwNjA2NzEyNX0.8uA7lyDtNNXqZYquo1S3yUNQxGcJVZKAqzyY3cPXRq0
```

`GET /api/v1/users/meetings/accept/:id`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "203",
    "type": "user_meetings",
    "attributes": {
      "non_compliance_action": null,
      "organizer_notes": null,
      "meeting_id": 203,
      "user_id": 798,
      "token": "844D87LX21QmDogK6BtJy1xB"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/users/meetings/accept/203" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhY2U4OWZiYi03ODI2LTQ1OWUtYjUxOC1hODhiOWZmMGIyZGUiLCJzdWIiOiI3OTgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjUsImV4cCI6MTYwNjA2NzEyNX0.8uA7lyDtNNXqZYquo1S3yUNQxGcJVZKAqzyY3cPXRq0"
```
## Convert meeting to focus block


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/193/make_focus_block?by_period[starts_at]=2020-10-28+17%3A45%3A21+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A21+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkYmY0ZDlmZC1iZTdiLTRiZTMtOGM3ZC0zMjE0ZjY1NGM4MWEiLCJzdWIiOiI3NzQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjEsImV4cCI6MTYwNjA2NzEyMX0.LMc3s-b9XjfFetaT14lVGvnLyGePeu6j3MNzhCiVTE4
```

`GET /api/v1/meetings/:id/make_focus_block`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:21 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:21 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "41",
    "type": "focus_blocks",
    "attributes": {
      "label": "Coding",
      "category": "focus",
      "calendar_id": 801,
      "recurring_meeting_uuid": "6vkb5i9kqmu36jr1t0v48lkcrk",
      "duration": 3600,
      "starts_at": "2020-10-26T22:03:00.000Z",
      "ends_at": "2020-10-26T23:03:00.000Z",
      "rrule": "RRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA",
      "recurring": true
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/193/make_focus_block?by_period[starts_at]=2020-10-28+17%3A45%3A21+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A21+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkYmY0ZDlmZC1iZTdiLTRiZTMtOGM3ZC0zMjE0ZjY1NGM4MWEiLCJzdWIiOiI3NzQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjEsImV4cCI6MTYwNjA2NzEyMX0.LMc3s-b9XjfFetaT14lVGvnLyGePeu6j3MNzhCiVTE4"
```
## Convert meeting to life block


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/194/make_life_block?by_period[starts_at]=2020-10-28+17%3A45%3A21+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A21+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNTlkNTIyYi1jNTU2LTRiNzgtYTQxMS1iOGU2NTM1MjQ1YmIiLCJzdWIiOiI3NzYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjEsImV4cCI6MTYwNjA2NzEyMX0.6lgy4qEDsjOBNs9sXKpvK1wFbNDYUXfBf5PAL5HxWos
```

`GET /api/v1/meetings/:id/make_life_block`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:21 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:21 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "42",
    "type": "focus_blocks",
    "attributes": {
      "label": "Coding",
      "category": "life",
      "calendar_id": 803,
      "recurring_meeting_uuid": "6vkb5i9kqmu36jr1t0v48lkcrk",
      "duration": 3600,
      "starts_at": "2020-10-26T22:03:00.000Z",
      "ends_at": "2020-10-26T23:03:00.000Z",
      "rrule": "RRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA",
      "recurring": true
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/194/make_life_block?by_period[starts_at]=2020-10-28+17%3A45%3A21+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A21+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNTlkNTIyYi1jNTU2LTRiNzgtYTQxMS1iOGU2NTM1MjQ1YmIiLCJzdWIiOiI3NzYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjEsImV4cCI6MTYwNjA2NzEyMX0.6lgy4qEDsjOBNs9sXKpvK1wFbNDYUXfBf5PAL5HxWos"
```
## List meetings


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings?by_period[starts_at]=2020-10-28+17%3A45%3A21+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A21+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMTBmNDdiMS1iYTVhLTQ1MGUtYmIyOS0xMWVkYmFkYWI2NjAiLCJzdWIiOiI3NzIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjEsImV4cCI6MTYwNjA2NzEyMX0.kN8FkPoXWGYs0MCc6pRrdX_8tDXKouXxaPEFSzojDEg
```

`GET /api/v1/meetings`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:21 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:21 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "192",
      "type": "meetings",
      "attributes": {
        "summary": "Authentic mlkshk pop-up cardigan normcore.",
        "description": "Ullam soluta ut. Et quia ullam. Iure enim sint. Officia sunt et.",
        "starts_at": "2020-10-28T17:50:20.969Z",
        "ends_at": "2020-10-28T18:50:20.969Z",
        "category_list": [

        ],
        "location": "3641 Schaefer Flat, Lake Brunilda, OR 77325-3794",
        "duration": 3600,
        "status": null,
        "wellness_block_id": null,
        "wellness_block_category": null,
        "event_report_card_id": null,
        "score": null,
        "recurring_meeting": false,
        "agenda_items": {
          "data": [

          ]
        },
        "objectives": {
          "data": [

          ]
        },
        "prework_items": {
          "data": [

          ]
        }
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings?by_period[starts_at]=2020-10-28+17%3A45%3A21+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A21+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMTBmNDdiMS1iYTVhLTQ1MGUtYmIyOS0xMWVkYmFkYWI2NjAiLCJzdWIiOiI3NzIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjEsImV4cCI6MTYwNjA2NzEyMX0.kN8FkPoXWGYs0MCc6pRrdX_8tDXKouXxaPEFSzojDEg"
```
## Meeting details for unauthenticated organizer


### Request

#### Endpoint

```plaintext
GET /api/v1/users/meetings/details/JGujWF8wKfaa76TuDt5budFs
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkYTgxYTg0Yy1lODQ2LTRjY2YtOTkxYi04YWE5ODUyMjU4ZWQiLCJzdWIiOiI4MDEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjUsImV4cCI6MTYwNjA2NzEyNX0.D-oFbT1Fcc6INctTXwqMtsWg9Di5-RMJjb7ifIBTYds
```

`GET /api/v1/users/meetings/details/:user_meeting_token`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "204",
    "type": "meetings",
    "attributes": {
      "summary": "Brooklyn butcher banh mi yolo squid irony cleanse swag.",
      "description": "Error est deserunt. Dolorem iste incidunt. Id qui rerum. Libero rerum ut.",
      "starts_at": "2020-10-28T17:50:25.597Z",
      "ends_at": "2020-10-28T18:50:25.597Z",
      "category_list": [

      ],
      "intention": null,
      "location": "74292 Luz Camp, West Rosalie, TN 20854-8428",
      "duration": 3600,
      "maybe_focus_block": false,
      "maybe_life_block": false,
      "status": null,
      "edit_permission": true,
      "wellness_block_id": null,
      "event_report_card_id": null,
      "compliance_deadline": "2020-10-28T11:50:25.597Z",
      "wellness_block_category": null,
      "details_negative": {
        "required_agenda": "This meeting needs an agenda",
        "required_objectives": "An objective is missing. What is the aim of the meeting? Understanding the goal for the meeting helps attendees engage.",
        "last_minute_schedule": "The invitee prefers more time before the meeting starts. A meeting scheduled last second usually means that the meeting could be better prepared.",
        "required_intention": "Missing a intention"
      },
      "details_positive": {
        "meeting_conflict": "There are no conflicts with any other meetings.",
        "max_attendees": "The number of attendees is acceptable.",
        "desired_duration": "This is an acceptable length of time."
      },
      "focus_blockable": false,
      "life_blockable": true,
      "attendees": [
        {
          "email": "brittany@leuschke-monahan.info",
          "domain": "leuschke-monahan.info",
          "role": "subject_matter_expert"
        },
        {
          "email": "tess.huels@buckridge.biz",
          "domain": "buckridge.biz",
          "role": "subject_matter_expert"
        }
      ],
      "attendees_count": 2,
      "cost": 76.0,
      "recurring_meeting": false,
      "score": 34,
      "results": null,
      "quality_label": "Now ask yourself, 'Is this a good use of my time?'",
      "agenda_items": {
        "data": [

        ]
      },
      "objectives": {
        "data": [

        ]
      },
      "prework_items": {
        "data": [

        ]
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/users/meetings/details/JGujWF8wKfaa76TuDt5budFs" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkYTgxYTg0Yy1lODQ2LTRjY2YtOTkxYi04YWE5ODUyMjU4ZWQiLCJzdWIiOiI4MDEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjUsImV4cCI6MTYwNjA2NzEyNX0.D-oFbT1Fcc6INctTXwqMtsWg9Di5-RMJjb7ifIBTYds"
```
## Organizer prevents a decline


### Request

#### Endpoint

```plaintext
PUT /api/v1/users/meetings/prevent_decline/tqpCbHb1YJt3DR2pF31wV9Wy
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNTU1MDZlOS01NzRjLTQ1M2ItOGYxNy01ZDI3NTA2YTMzMTEiLCJzdWIiOiI4MDQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjYsImV4cCI6MTYwNjA2NzEyNn0.2gnjQufmcgEOzVpLzEk9PIROU89lq-FAeV5FsvfPE4A
```

`PUT /api/v1/users/meetings/prevent_decline/:user_meeting_token`

#### Parameters


```json
{"data":{"type":"user_meeting","attributes":{"organizer_notes":"Testing!"}}}
```

None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "205",
    "type": "user_meetings",
    "attributes": {
      "non_compliance_action": "do nothing",
      "organizer_notes": "Testing!",
      "meeting_id": 205,
      "user_id": 804,
      "token": "tqpCbHb1YJt3DR2pF31wV9Wy"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/users/meetings/prevent_decline/tqpCbHb1YJt3DR2pF31wV9Wy" -d '{"data":{"type":"user_meeting","attributes":{"organizer_notes":"Testing!"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNTU1MDZlOS01NzRjLTQ1M2ItOGYxNy01ZDI3NTA2YTMzMTEiLCJzdWIiOiI4MDQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjYsImV4cCI6MTYwNjA2NzEyNn0.2gnjQufmcgEOzVpLzEk9PIROU89lq-FAeV5FsvfPE4A"
```
## Show meeting evaluation


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/191/evaluate?by_period[starts_at]=2020-10-28+17%3A45%3A20+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A20+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjN2FiOWM2NS1iMzI3LTQ2MTItYjAyYi1jMDZmYzMwMmVhY2MiLCJzdWIiOiI3NzAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjAsImV4cCI6MTYwNjA2NzEyMH0.VJd3-Q50gfROmUVgjflPS5jzoCSCMrw_a4JaakcwhCE
```

`GET /api/v1/meetings/:id/evaluate`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:20 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:20 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "191",
    "type": "meetings",
    "attributes": {
      "summary": "Mlkshk keytar yolo vinyl blog selvage austin.",
      "description": "Autem est rerum. Illo doloremque tempore. Voluptas corporis eos. Sed et est.",
      "starts_at": "2020-10-28T17:50:20.606Z",
      "ends_at": "2020-10-28T18:50:20.606Z",
      "category_list": [

      ],
      "intention": null,
      "location": "6177 Nicholas Divide, Muellerburgh, KS 85212",
      "duration": 3600,
      "maybe_focus_block": false,
      "maybe_life_block": false,
      "status": null,
      "edit_permission": true,
      "wellness_block_id": null,
      "event_report_card_id": null,
      "compliance_deadline": null,
      "wellness_block_category": null,
      "details_negative": null,
      "details_positive": null,
      "focus_blockable": false,
      "life_blockable": true,
      "attendees": [
        {
          "email": "darrin_koch@murphy.org",
          "domain": "murphy.org",
          "role": "subject_matter_expert"
        }
      ],
      "attendees_count": 1,
      "cost": 38.0,
      "recurring_meeting": false,
      "score": null,
      "results": null,
      "quality_label": null,
      "agenda_items": {
        "data": [

        ]
      },
      "objectives": {
        "data": [

        ]
      },
      "prework_items": {
        "data": [

        ]
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/191/evaluate?by_period[starts_at]=2020-10-28+17%3A45%3A20+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A20+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjN2FiOWM2NS1iMzI3LTQ2MTItYjAyYi1jMDZmYzMwMmVhY2MiLCJzdWIiOiI3NzAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjAsImV4cCI6MTYwNjA2NzEyMH0.VJd3-Q50gfROmUVgjflPS5jzoCSCMrw_a4JaakcwhCE"
```
## Show user meeting


### Request

#### Endpoint

```plaintext
GET /api/v1/users/meetings/202
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxNWJlNGRjNi04MDBjLTRiYTItODBkZC0zOGFjNDE2YjU1ZjAiLCJzdWIiOiI3OTUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjUsImV4cCI6MTYwNjA2NzEyNX0.7iqtAm4AgS8s2kCvvC8LT4tY_hlvKXtcg3qKg_RanHc
```

`GET /api/v1/users/meetings/:id`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "202",
    "type": "user_meetings",
    "attributes": {
      "non_compliance_action": null,
      "organizer_notes": null,
      "meeting_id": 202,
      "user_id": 795,
      "token": "uH7YNsRAD4JitU53agKkk4AU"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/users/meetings/202" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxNWJlNGRjNi04MDBjLTRiYTItODBkZC0zOGFjNDE2YjU1ZjAiLCJzdWIiOiI3OTUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjUsImV4cCI6MTYwNjA2NzEyNX0.7iqtAm4AgS8s2kCvvC8LT4tY_hlvKXtcg3qKg_RanHc"
```
## Update meeting


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/195
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzZTkxYzg2OC1iMjQ3LTQ3N2ItYTI5Mi03ZWIyMzI5OTg2YzkiLCJzdWIiOiI3NzgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjIsImV4cCI6MTYwNjA2NzEyMn0.RGmWQih-I4mQ4nN_J9N05Xlyu40Q8rhgMbvYYUlQias
```

`PUT /api/v1/meetings/:id`

#### Parameters


```json
{"by_period":{"starts_at":"2020-10-28T17:45:22.161Z","ends_at":"2020-11-04T17:45:22.161Z"},"data":{"type":"agenda_item","attributes":{"started_at":"2020-10-28T17:25:22.161Z","ended_at":"2020-10-28T17:45:22.161Z"}}}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| started_at  |  started at |
| ended_at  |  ended at |
| time_spent_in_secs  |  time spent in secs |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "195",
    "type": "meetings",
    "attributes": {
      "summary": "Vhs fashion axe biodiesel post-ironic.",
      "description": "Et sit autem. Doloribus eum et. Qui perferendis cumque. Sint ad illum.",
      "starts_at": "2020-10-28T17:50:22.002Z",
      "ends_at": "2020-10-28T18:50:22.002Z",
      "category_list": [

      ],
      "intention": null,
      "location": "Apt. 177 76340 Gusikowski Prairie, Lake Nevilleburgh, VA 50087-8468",
      "duration": 3600,
      "maybe_focus_block": false,
      "maybe_life_block": false,
      "status": null,
      "edit_permission": true,
      "wellness_block_id": null,
      "event_report_card_id": null,
      "compliance_deadline": null,
      "wellness_block_category": null,
      "details_negative": null,
      "details_positive": null,
      "focus_blockable": false,
      "life_blockable": true,
      "attendees": [
        {
          "email": "jestine_kohler@zboncak-thompson.biz",
          "domain": "zboncak-thompson.biz",
          "role": "subject_matter_expert"
        }
      ],
      "attendees_count": 1,
      "cost": 38.0,
      "recurring_meeting": false,
      "score": null,
      "results": null,
      "quality_label": null,
      "agenda_items": {
        "data": [

        ]
      },
      "objectives": {
        "data": [

        ]
      },
      "prework_items": {
        "data": [

        ]
      }
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/195" -d '{"by_period":{"starts_at":"2020-10-28T17:45:22.161Z","ends_at":"2020-11-04T17:45:22.161Z"},"data":{"type":"agenda_item","attributes":{"started_at":"2020-10-28T17:25:22.161Z","ended_at":"2020-10-28T17:45:22.161Z"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzZTkxYzg2OC1iMjQ3LTQ3N2ItYTI5Mi03ZWIyMzI5OTg2YzkiLCJzdWIiOiI3NzgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjIsImV4cCI6MTYwNjA2NzEyMn0.RGmWQih-I4mQ4nN_J9N05Xlyu40Q8rhgMbvYYUlQias"
```
## Update user meeting


### Request

#### Endpoint

```plaintext
PUT /api/v1/users/meetings/201
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5OTYxMmNmZS1jNDAwLTQ2ZDMtYWI4NC05N2RiZDYwMGU4NjQiLCJzdWIiOiI3OTIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjQsImV4cCI6MTYwNjA2NzEyNH0.sSrzOrzE6TyKVOfSTSqLniV4x_iTmHNWKQvMUDbKGXM
```

`PUT /api/v1/users/meetings/:id`

#### Parameters


```json
{"data":{"type":"user_meeting","attributes":{"non_compliance_action":"decline"}}}
```


| Name | Description |
|:-----|:------------|
| non_compliance_action *required* | remind, decline, etc |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "201",
    "type": "user_meetings",
    "attributes": {
      "non_compliance_action": "decline",
      "organizer_notes": null,
      "meeting_id": 201,
      "user_id": 792,
      "token": "EHbgFhvYi3Wyz76MZVLWbP3v"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/users/meetings/201" -d '{"data":{"type":"user_meeting","attributes":{"non_compliance_action":"decline"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5OTYxMmNmZS1jNDAwLTQ2ZDMtYWI4NC05N2RiZDYwMGU4NjQiLCJzdWIiOiI3OTIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjQsImV4cCI6MTYwNjA2NzEyNH0.sSrzOrzE6TyKVOfSTSqLniV4x_iTmHNWKQvMUDbKGXM"
```
# Microsoft Outlook



## List Outlook Calendars


### Request

#### Endpoint

```plaintext
GET /api/v1/microsoft_outlook/list
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkOTZkYjI1MC0yM2JlLTQxZmEtOWQ1NC1iZDBiOThhODUzYjQiLCJzdWIiOiI4MTQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.wob8HWRfOrv5FVsmj_dK7OW73t5ezxnRSjZa-852TTM
```

`GET /api/v1/microsoft_outlook/list`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "AQMkADAwATM0MDAAMS0yMWI4LWMzYTktMDACLTAwCgBGAAAD05FBgSzQMkOHu1sf5cDnwAcAduHsdxvLcUmEsBp_QJ5q8gAAAgEGAAAAduHsdxvLcUmEsBp_QJ5q8gAAAmhcAAAA",
      "type": "external_calendars",
      "attributes": {
        "name": "Calendar",
        "primary": true,
        "deleted": null
      }
    },
    {
      "id": "AQMkADAwATM0MDAAMS0yMWI4LWMzYTktMDACLTAwCgBGAAAD05FBgSzQMkOHu1sf5cDnwAcAduHsdxvLcUmEsBp_QJ5q8gAAAgEGAAAAduHsdxvLcUmEsBp_QJ5q8gAAAmhhAAAA",
      "type": "external_calendars",
      "attributes": {
        "name": "United States holidays",
        "primary": false,
        "deleted": null
      }
    },
    {
      "id": "AQMkADAwATM0MDAAMS0yMWI4LWMzYTktMDACLTAwCgBGAAAD05FBgSzQMkOHu1sf5cDnwAcAduHsdxvLcUmEsBp_QJ5q8gAAAgEGAAAAduHsdxvLcUmEsBp_QJ5q8gAAAmhiAAAA",
      "type": "external_calendars",
      "attributes": {
        "name": "Birthdays",
        "primary": false,
        "deleted": null
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/microsoft_outlook/list" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkOTZkYjI1MC0yM2JlLTQxZmEtOWQ1NC1iZDBiOThhODUzYjQiLCJzdWIiOiI4MTQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.wob8HWRfOrv5FVsmj_dK7OW73t5ezxnRSjZa-852TTM"
```
## Setup Outlook Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/microsoft_outlook/webhooks_setup
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlOTJmZTljMS1iNzBiLTQ3NWMtODk4Mi1iY2IxNWI1NmY1YTAiLCJzdWIiOiI4MjQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjgsImV4cCI6MTYwNjA2NzEyOH0.iB0WNz1EYIHAZGMZczN74C_vJQ4RtElSz0P13b6gAOQ
```

`POST /api/v1/microsoft_outlook/webhooks_setup`

#### Parameters


```json
{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| calendar_uuid *required* | Outlook Calendar UUID |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/microsoft_outlook/webhooks_setup" -d '{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlOTJmZTljMS1iNzBiLTQ3NWMtODk4Mi1iY2IxNWI1NmY1YTAiLCJzdWIiOiI4MjQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjgsImV4cCI6MTYwNjA2NzEyOH0.iB0WNz1EYIHAZGMZczN74C_vJQ4RtElSz0P13b6gAOQ"
```
## Stop Outlook Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/microsoft_outlook/webhooks_stop
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3ODg3ZjQ3Mi1mNmM0LTQxMGMtOGI0MS01NzJjMmM4YWNkYzciLCJzdWIiOiI4MjciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.tS1Hxihss7t1L3eW05X_Mbt2nTlejvzlpwE-YwjJBxU
```

`POST /api/v1/microsoft_outlook/webhooks_stop`

#### Parameters


```json
{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| calendar_uuid *required* | Outlook Calendar UUID |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/microsoft_outlook/webhooks_stop" -d '{"calendar_uuid":"test@test.com","data":{"type":"calendars","attributes":{"calendar_uuid":"test@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3ODg3ZjQ3Mi1mNmM0LTQxMGMtOGI0MS01NzJjMmM4YWNkYzciLCJzdWIiOiI4MjciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.tS1Hxihss7t1L3eW05X_Mbt2nTlejvzlpwE-YwjJBxU"
```
## Watch Outlook Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/microsoft_outlook/events/watch
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxNjgzNWM0Ny1hMmEyLTRhMzQtYjcxOC1lNzBhNTkxMmNmNjQiLCJzdWIiOiI4MjUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.4fE6zhcdxS9ptMsLMoG20NZsHsU4oe2-ezXkfYrEkTw
```

`POST /api/v1/microsoft_outlook/events/watch`

#### Parameters


```json
{"value":[{"clientState":"ad37d01b-f6de-4f93-b7a3-279d83a463f9","subscriptionId":"eedb1ff5-2fd8-4b45-a2cc-59a06cfdbe59"}]}
```


| Name | Description |
|:-----|:------------|
| value *required* |  value |



### Response

```plaintext
Content-Type: text/plain; charset=utf-8
202 Accepted
```


```json
 
```



```shell
curl "http://localhost:3000/api/v1/microsoft_outlook/events/watch" -d '{"value":[{"clientState":"ad37d01b-f6de-4f93-b7a3-279d83a463f9","subscriptionId":"eedb1ff5-2fd8-4b45-a2cc-59a06cfdbe59"}]}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxNjgzNWM0Ny1hMmEyLTRhMzQtYjcxOC1lNzBhNTkxMmNmNjQiLCJzdWIiOiI4MjUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.4fE6zhcdxS9ptMsLMoG20NZsHsU4oe2-ezXkfYrEkTw"
```
## Watch Outlook Webhook Lifecycle


### Request

#### Endpoint

```plaintext
POST /api/v1/microsoft_outlook/events/lifecycle
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0OTg1NGM3Ny03MmYyLTRmMGYtYmU2My02MzBhY2RiY2JkMjUiLCJzdWIiOiI4MjIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjgsImV4cCI6MTYwNjA2NzEyOH0.MYWyWWk9Hty1YVFik04A24SBPVAuoAQ2yXr1ZFV1p9g
```

`POST /api/v1/microsoft_outlook/events/lifecycle`

#### Parameters


```json
{"value":[{"clientState":"6a387ff0-dbac-4612-bd71-c30603034837","subscriptionId":"ae2ee49c-c1cc-4bb4-af06-61d65dae7da8"}]}
```


| Name | Description |
|:-----|:------------|
| validationToken  | Validation Token |
| value *required* |  value |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/microsoft_outlook/events/lifecycle" -d '{"value":[{"clientState":"6a387ff0-dbac-4612-bd71-c30603034837","subscriptionId":"ae2ee49c-c1cc-4bb4-af06-61d65dae7da8"}]}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0OTg1NGM3Ny03MmYyLTRmMGYtYmU2My02MzBhY2RiY2JkMjUiLCJzdWIiOiI4MjIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjgsImV4cCI6MTYwNjA2NzEyOH0.MYWyWWk9Hty1YVFik04A24SBPVAuoAQ2yXr1ZFV1p9g"
```
# Objectives



## Create objective


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/180/objectives
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4ZTk4ZTM2NC05ZWUwLTRkMjctODNkYi0yYWU3OTU2YTkxY2EiLCJzdWIiOiI3MjUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTQsImV4cCI6MTYwNjA2NzExNH0._qIAYIkx5sI3jLz90N53OvWx9_zHbWTHTNwqEiBGDrc
```

`POST /api/v1/meetings/:meeting_id/objectives`

#### Parameters


```json
{"data":{"type":"objective","attributes":{"description":"Figure something out","position":3}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "36",
    "type": "objectives",
    "attributes": {
      "meeting_id": 180,
      "description": "Figure something out",
      "position": 3
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/180/objectives" -d '{"data":{"type":"objective","attributes":{"description":"Figure something out","position":3}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4ZTk4ZTM2NC05ZWUwLTRkMjctODNkYi0yYWU3OTU2YTkxY2EiLCJzdWIiOiI3MjUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTQsImV4cCI6MTYwNjA2NzExNH0._qIAYIkx5sI3jLz90N53OvWx9_zHbWTHTNwqEiBGDrc"
```
## Delete objective


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/179/objectives/34
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhZTc2MTYwMi03MjM1LTRkODEtYWU2YS04NTJlOTEzNGI4NDciLCJzdWIiOiI3MjQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTQsImV4cCI6MTYwNjA2NzExNH0.5g9STtn3u7C7V1d820e6RcQCn03aoQllzEcE5YZyoF8
```

`DELETE /api/v1/meetings/:meeting_id/objectives/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/meetings/179/objectives/34" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhZTc2MTYwMi03MjM1LTRkODEtYWU2YS04NTJlOTEzNGI4NDciLCJzdWIiOiI3MjQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTQsImV4cCI6MTYwNjA2NzExNH0.5g9STtn3u7C7V1d820e6RcQCn03aoQllzEcE5YZyoF8"
```
## List objectives


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/177/objectives
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMzdhN2RlOS0xZGM3LTRhYjgtYjY1Ni1iMDAwMTZlZTE0Y2UiLCJzdWIiOiI3MjIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTQsImV4cCI6MTYwNjA2NzExNH0.h2HNXWwvMtn0IxMpQD65sgNyUkyP9HomJtjUh59ShVA
```

`GET /api/v1/meetings/:meeting_id/objectives`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "32",
      "type": "objectives",
      "attributes": {
        "meeting_id": 177,
        "description": "Cliche banjo semiotics thundercats next level tattooed single-origin coffee selvage messenger bag pabst.",
        "position": null
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/177/objectives" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMzdhN2RlOS0xZGM3LTRhYjgtYjY1Ni1iMDAwMTZlZTE0Y2UiLCJzdWIiOiI3MjIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTQsImV4cCI6MTYwNjA2NzExNH0.h2HNXWwvMtn0IxMpQD65sgNyUkyP9HomJtjUh59ShVA"
```
## Show objective


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/178/objectives/33
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5ODcyYTg2OS00ZDY3LTQyZjgtYmE1YS0zOTJlNzUyMGQyOTYiLCJzdWIiOiI3MjMiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTQsImV4cCI6MTYwNjA2NzExNH0.yqWtwj9Zn9VBRojVfUbaf4Alikc3xG1bSaNt-dkwO1Q
```

`GET /api/v1/meetings/:meeting_id/objectives/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "33",
    "type": "objectives",
    "attributes": {
      "meeting_id": 178,
      "description": "Viral ennui retro dreamcatcher readymade messenger bag etsy cold-pressed.",
      "position": null
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/178/objectives/33" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5ODcyYTg2OS00ZDY3LTQyZjgtYmE1YS0zOTJlNzUyMGQyOTYiLCJzdWIiOiI3MjMiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTQsImV4cCI6MTYwNjA2NzExNH0.yqWtwj9Zn9VBRojVfUbaf4Alikc3xG1bSaNt-dkwO1Q"
```
## Update objective


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/176/objectives/31
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4OGQ2ZWI1MC01NTZhLTQ4Y2EtOTVkMS1jZjZlNTVkZmYxZDUiLCJzdWIiOiI3MjEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTMsImV4cCI6MTYwNjA2NzExM30.m4zgalSOJiBt2xTs-AilFsF7b7nG3AMz_Ts0JSQFtxM
```

`PUT /api/v1/meetings/:meeting_id/objectives/:id`

#### Parameters


```json
{"data":{"type":"objective","attributes":{"description":"Figure it all out"}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| position  | Position for sorting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "31",
    "type": "objectives",
    "attributes": {
      "meeting_id": 176,
      "description": "Figure it all out",
      "position": null
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/176/objectives/31" -d '{"data":{"type":"objective","attributes":{"description":"Figure it all out"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4OGQ2ZWI1MC01NTZhLTQ4Y2EtOTVkMS1jZjZlNTVkZmYxZDUiLCJzdWIiOiI3MjEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTMsImV4cCI6MTYwNjA2NzExM30.m4zgalSOJiBt2xTs-AilFsF7b7nG3AMz_Ts0JSQFtxM"
```
# Organizer Deny-List



## Bulk create deny-list entries


### Request

#### Endpoint

```plaintext
POST /api/v1/users/blacklist_organizers/bulk
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhYjIyMGZiZC0yMDY4LTRjM2ItODViYS03NmEzMjBjMzZkZmUiLCJzdWIiOiI3NTkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTksImV4cCI6MTYwNjA2NzExOX0.Wdv3jvA3Zs4u1ik4vru_ONSyyY6Fu_f_FmBHa5CWOKE
```

`POST /api/v1/users/blacklist_organizers/bulk`

#### Parameters


```json
{"data":{"type":"attendee","attributes":{"email_list":"test@test.com,test2@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| email_list *required* |  email list |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": [
    {
      "id": "22",
      "type": "blacklist_organizers",
      "attributes": {
        "email": "test@test.com"
      }
    },
    {
      "id": "23",
      "type": "blacklist_organizers",
      "attributes": {
        "email": "test2@test.com"
      }
    }
  ]
}
```



```shell
curl "http://localhost:3000/api/v1/users/blacklist_organizers/bulk" -d '{"data":{"type":"attendee","attributes":{"email_list":"test@test.com,test2@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhYjIyMGZiZC0yMDY4LTRjM2ItODViYS03NmEzMjBjMzZkZmUiLCJzdWIiOiI3NTkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTksImV4cCI6MTYwNjA2NzExOX0.Wdv3jvA3Zs4u1ik4vru_ONSyyY6Fu_f_FmBHa5CWOKE"
```
## Create deny-list entry


### Request

#### Endpoint

```plaintext
POST /api/v1/users/blacklist_organizers
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0ZWI3ZWJkMy1jZWMzLTQ2NjUtOGM3Yy0xN2U5YzY1ZGJkNGIiLCJzdWIiOiI3NjEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTksImV4cCI6MTYwNjA2NzExOX0.su1Q1ps527SJrjr0jBoDCi7z8f1fW_XmKWSOhQPSNh8
```

`POST /api/v1/users/blacklist_organizers`

#### Parameters


```json
{"data":{"type":"attendee","attributes":{"email":"test@test.com"}}}
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "24",
    "type": "blacklist_organizers",
    "attributes": {
      "email": "test@test.com"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/users/blacklist_organizers" -d '{"data":{"type":"attendee","attributes":{"email":"test@test.com"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0ZWI3ZWJkMy1jZWMzLTQ2NjUtOGM3Yy0xN2U5YzY1ZGJkNGIiLCJzdWIiOiI3NjEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTksImV4cCI6MTYwNjA2NzExOX0.su1Q1ps527SJrjr0jBoDCi7z8f1fW_XmKWSOhQPSNh8"
```
## List denied organizers


### Request

#### Endpoint

```plaintext
GET /api/v1/users/blacklist_organizers
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzOWZkODUxZS03ZTRjLTRjOWUtOWUzZi1mMTdmOThkZTZkZjEiLCJzdWIiOiI3NjAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTksImV4cCI6MTYwNjA2NzExOX0.wDYqJAHo8JBz3IdYDnX-sIAO8hCPuGEa0HCc6njXaW0
```

`GET /api/v1/users/blacklist_organizers`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/users/blacklist_organizers" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzOWZkODUxZS03ZTRjLTRjOWUtOWUzZi1mMTdmOThkZTZkZjEiLCJzdWIiOiI3NjAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTksImV4cCI6MTYwNjA2NzExOX0.wDYqJAHo8JBz3IdYDnX-sIAO8hCPuGEa0HCc6njXaW0"
```
## Remove denied organizer


### Request

#### Endpoint

```plaintext
DELETE /api/v1/users/blacklist_organizers/21
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNGY3ZWQyOS02OTEyLTQ1YWQtOGI2Yi03MTg4MjMyZGNhNGIiLCJzdWIiOiI3NTgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.gGm-1eXBbqm_BA4fK9wq15e7MaszXWOnIk1WktPqC0g
```

`DELETE /api/v1/users/blacklist_organizers/:id`

#### Parameters


None known.


### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/users/blacklist_organizers/21" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNGY3ZWQyOS02OTEyLTQ1YWQtOGI2Yi03MTg4MjMyZGNhNGIiLCJzdWIiOiI3NTgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.gGm-1eXBbqm_BA4fK9wq15e7MaszXWOnIk1WktPqC0g"
```
# Ping



## Authenticated Ping


### Request

#### Endpoint

```plaintext
GET /api/v1/ping
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NWVhZDM3MS1kYzkxLTQxYWUtYmVjNC03YmEyYzJmOTM3ZGYiLCJzdWIiOiI3MjciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTQsImV4cCI6MTYwNjA2NzExNH0.p5tbXofxGMAtLe5SCVXuxSimbKQrg2wnXXhSQ_q5NxE
```

`GET /api/v1/ping`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "157db283-2d33-443e-b1dc-46af22e1a66d",
    "type": "pings",
    "attributes": {
      "id": "157db283-2d33-443e-b1dc-46af22e1a66d",
      "date": "2020-10-28T17:45:14.917Z"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/ping" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NWVhZDM3MS1kYzkxLTQxYWUtYmVjNC03YmEyYzJmOTM3ZGYiLCJzdWIiOiI3MjciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTQsImV4cCI6MTYwNjA2NzExNH0.p5tbXofxGMAtLe5SCVXuxSimbKQrg2wnXXhSQ_q5NxE"
```
# Pre-Work Items



## Create prework item


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/210/prework_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2MjIzNzU2YS1iYTA1LTQ0OWItOWMzYS1hNTZmYjY3NmM0ZjMiLCJzdWIiOiI4MTEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.TwThKHk4pj1Al0rcygziY6dYvWa4IMytHiOWeUukJ6I
```

`POST /api/v1/meetings/:meeting_id/prework_items`

#### Parameters


```json
{"data":{"type":"prework_item","attributes":{"description":"Review the sales report","url":"https://www.locationtofile.com/salesreport.xls","timebox":3600}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| timebox  | Max amount of time that should be spent in seconds |
| url  |  url |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "24",
    "type": "prework_items",
    "attributes": {
      "id": 24,
      "description": "Review the sales report",
      "url": "https://www.locationtofile.com/salesreport.xls",
      "timebox": 3600
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/210/prework_items" -d '{"data":{"type":"prework_item","attributes":{"description":"Review the sales report","url":"https://www.locationtofile.com/salesreport.xls","timebox":3600}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2MjIzNzU2YS1iYTA1LTQ0OWItOWMzYS1hNTZmYjY3NmM0ZjMiLCJzdWIiOiI4MTEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.TwThKHk4pj1Al0rcygziY6dYvWa4IMytHiOWeUukJ6I"
```
## Delete prework item


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/206/prework_items/21
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmMGQ3ZDM3Zi1jNzVmLTRmZTAtODk1MC0zZmY4YzhjMzBhNzgiLCJzdWIiOiI4MDciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjYsImV4cCI6MTYwNjA2NzEyNn0.4s5zJbpYcQTIfD722vmvKWpHqJCPR3kt1k36cR3XMhY
```

`DELETE /api/v1/meetings/:meeting_id/prework_items/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| timebox  | Max amount of time that should be spent in seconds |
| url  |  url |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/meetings/206/prework_items/21" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmMGQ3ZDM3Zi1jNzVmLTRmZTAtODk1MC0zZmY4YzhjMzBhNzgiLCJzdWIiOiI4MDciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjYsImV4cCI6MTYwNjA2NzEyNn0.4s5zJbpYcQTIfD722vmvKWpHqJCPR3kt1k36cR3XMhY"
```
## List prework items


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/208/prework_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjMDliMmI5My1mNmQwLTRlZjYtOTIxZC1mY2U1MzU0YTQ1MTUiLCJzdWIiOiI4MDkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjYsImV4cCI6MTYwNjA2NzEyNn0.CmxomoVNoUA0_f_jMbBUShMlDFOS4xjf4_eQM4DaxVA
```

`GET /api/v1/meetings/:meeting_id/prework_items`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| timebox  | Max amount of time that should be spent in seconds |
| url  |  url |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/208/prework_items" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjMDliMmI5My1mNmQwLTRlZjYtOTIxZC1mY2U1MzU0YTQ1MTUiLCJzdWIiOiI4MDkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjYsImV4cCI6MTYwNjA2NzEyNn0.CmxomoVNoUA0_f_jMbBUShMlDFOS4xjf4_eQM4DaxVA"
```
## Show prework item


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/209/prework_items/23
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkY2YzNDExNC1jMjU5LTQ0NTUtODU1Ni03Nzk5YjI2OTE5ODgiLCJzdWIiOiI4MTAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.nUpsjuXmNlBKow1jZEitO_zFUVmvVZWISBWt-1wV1BA
```

`GET /api/v1/meetings/:meeting_id/prework_items/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| description *required* |  description |
| timebox  | Max amount of time that should be spent in seconds |
| url  |  url |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "23",
    "type": "prework_items",
    "attributes": {
      "id": 23,
      "description": "Muggle magic shoreditch schlitz brooklyn waistcoat trust fund tofu.",
      "url": "http://gleason-bosco.org/jeffrey_oberbrunner",
      "timebox": 3600
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/209/prework_items/23" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkY2YzNDExNC1jMjU5LTQ0NTUtODU1Ni03Nzk5YjI2OTE5ODgiLCJzdWIiOiI4MTAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.nUpsjuXmNlBKow1jZEitO_zFUVmvVZWISBWt-1wV1BA"
```
## Update prework item


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/207/prework_items/22
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3NmEyZWZlNy0xZTYzLTRhZWEtODlhMy0xMjFjN2E5NjcxYzciLCJzdWIiOiI4MDgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjYsImV4cCI6MTYwNjA2NzEyNn0.OeHqMwiuzY-nc5v_9yULPy-tNL10BFfeMgCpCz0VnkA
```

`PUT /api/v1/meetings/:meeting_id/prework_items/:id`

#### Parameters


```json
{"data":{"type":"prework_item","attributes":{"description":"Review the sales report dude"}}}
```


| Name | Description |
|:-----|:------------|
| description *required* |  description |
| timebox  | Max amount of time that should be spent in seconds |
| url  |  url |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "22",
    "type": "prework_items",
    "attributes": {
      "id": 22,
      "description": "Review the sales report dude",
      "url": "http://stiedemann-abernathy.co/ethan",
      "timebox": 3600
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/207/prework_items/22" -d '{"data":{"type":"prework_item","attributes":{"description":"Review the sales report dude"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3NmEyZWZlNy0xZTYzLTRhZWEtODlhMy0xMjFjN2E5NjcxYzciLCJzdWIiOiI4MDgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjYsImV4cCI6MTYwNjA2NzEyNn0.OeHqMwiuzY-nc5v_9yULPy-tNL10BFfeMgCpCz0VnkA"
```
# Reporting

Meeting Evaluation Reporting

## Average Number of Attendees


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/average_attendees?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjNTdmMjhlMi00ZTMwLTQ5ZGMtYWJiYS0xNDc5YzUwMTI0ZWUiLCJzdWIiOiI4MzMiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.ljh4_ceD6NlqUSlmYEYb9hxxR4Po2Il5_JQb9GERQZo
```

`GET /api/v1/reporting/user/evaluations/average_attendees`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:29 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:29 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "548f2319-0cc7-4494-abff-a4e0a2fe17fb",
    "type": "reports",
    "attributes": {
      "name": "Attendees",
      "starts_at": "2020-10-28T00:00:00.000Z",
      "ends_at": "2020-11-04T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
      },
      "trends": null,
      "average": null,
      "total": 0.0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/average_attendees?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjNTdmMjhlMi00ZTMwLTQ5ZGMtYWJiYS0xNDc5YzUwMTI0ZWUiLCJzdWIiOiI4MzMiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.ljh4_ceD6NlqUSlmYEYb9hxxR4Po2Il5_JQb9GERQZo"
```
## Average scores per evaluator


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/averages?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2ZmY0NDE1MC02MmQ2LTQ4YWUtOGQ2YS1kOTAwM2VjMTMxYTciLCJzdWIiOiI4MjkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.BEcWD3OcS2_lqOYny2_9AkWONk1PvyBzhzRDIQCbuPU
```

`GET /api/v1/reporting/user/evaluations/averages`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:29 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:29 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "ca0f9385-e8f8-4f36-a177-d2592963889d",
    "type": "reports",
    "attributes": {
      "name": "Evaluation averages and totals",
      "starts_at": "2020-10-28T00:00:00.000Z",
      "ends_at": "2020-11-04T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
        "totals": {
          "compliant": 0.0,
          "non_compliant": 0.0,
          "duration": 0.0
        },
        "counts": {
          "good": {
          },
          "bad": {
          }
        },
        "quality_label": "When it comes to your time - you deserve much better than this."
      },
      "trends": null,
      "average": 0.0,
      "total": 0.0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/averages?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2ZmY0NDE1MC02MmQ2LTQ4YWUtOGQ2YS1kOTAwM2VjMTMxYTciLCJzdWIiOiI4MjkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.BEcWD3OcS2_lqOYny2_9AkWONk1PvyBzhzRDIQCbuPU"
```
## Company User Counts


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/team/evaluations/user_counts?by_period[starts_at]=2020-10-28+17%3A45%3A14+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A14+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiMTdiNzZkNS0wMWQ1LTQxYjEtOWE5OS0yNzVlYTY3MDMyMmYiLCJzdWIiOiI3MjYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTQsImV4cCI6MTYwNjA2NzExNH0.r0gpY8CQIpi4mrac5CaG_yiKJ1WhBLnbfX_435_HAL8
```

`GET /api/v1/reporting/team/evaluations/user_counts`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:14 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:14 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "b76b5cc0-bffa-48a0-8747-9d7f7227c322",
    "type": "reports",
    "attributes": {
      "name": "Team User Count",
      "starts_at": "2020-10-28T00:00:00.000Z",
      "ends_at": "2020-11-04T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
        "evaluatable_users": 0,
        "total_users": 1
      },
      "trends": null,
      "average": 0,
      "total": 0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/team/evaluations/user_counts?by_period[starts_at]=2020-10-28+17%3A45%3A14+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A14+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiMTdiNzZkNS0wMWQ1LTQxYjEtOWE5OS0yNzVlYTY3MDMyMmYiLCJzdWIiOiI3MjYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTQsImV4cCI6MTYwNjA2NzExNH0.r0gpY8CQIpi4mrac5CaG_yiKJ1WhBLnbfX_435_HAL8"
```
## Duration and Cost Details


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/duration_and_cost_details?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjYTczODJhNy1mNDhmLTQwY2QtYjM0Ny1jMjExMWJiOWYyNDciLCJzdWIiOiI4MjgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.cslUuU09WUMnb3mbu662TaISLu1LOWIrAiVaWHf0lBw
```

`GET /api/v1/reporting/user/evaluations/duration_and_cost_details`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:29 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:29 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "77f06301-c807-4bdf-96d2-a6b355871506",
    "type": "reports",
    "attributes": {
      "name": "Duration and Costs Details",
      "starts_at": "2020-10-28T00:00:00.000Z",
      "ends_at": "2020-11-04T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
        "categories": {
        },
        "intentions": {
        }
      },
      "trends": null,
      "average": 0,
      "total": 0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/duration_and_cost_details?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjYTczODJhNy1mNDhmLTQwY2QtYjM0Ny1jMjExMWJiOWYyNDciLCJzdWIiOiI4MjgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.cslUuU09WUMnb3mbu662TaISLu1LOWIrAiVaWHf0lBw"
```
## Duration and Costs


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/duration_and_costs?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5YjY5ZTcwMi1kMTljLTRiMjktOGI2MS03ZWVhYmZlYmQ1YTkiLCJzdWIiOiI4MzAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.brhDI7M78nPYW4GW_r1XZ1vmf5AXQX5YxU83M-67UtQ
```

`GET /api/v1/reporting/user/evaluations/duration_and_costs`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:29 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:29 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "80fe5704-1fb8-4eac-9282-d70208a6808e",
    "type": "reports",
    "attributes": {
      "name": "Duration and Costs Summary",
      "starts_at": "2020-10-28T00:00:00.000Z",
      "ends_at": "2020-11-04T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
        "annual_salary": 75000,
        "estimated_hourly_pay": 38,
        "good": {
          "meetings": 0,
          "meeting_duration": 0,
          "attendee_total": 0,
          "ave_attendee_per_meeting": 0.0,
          "meeting_cost_total": 0.0,
          "meeting_cost_per_hour": null,
          "ave_cost_per_meeting": null
        },
        "bad": {
          "meetings": 0,
          "meeting_duration": 0,
          "attendee_total": 0,
          "ave_attendee_per_meeting": 0.0,
          "meeting_cost_total": 0.0,
          "meeting_cost_per_hour": null,
          "ave_cost_per_meeting": null
        },
        "total": {
          "meetings": 0,
          "meeting_duration": 0,
          "ave_meeting_duration": 0,
          "attendee_total": 0,
          "ave_attendee_per_meeting": 0.0,
          "meeting_cost_total": 0.0,
          "meeting_cost_per_hour": null,
          "ave_cost_per_meeting": null,
          "work_hours": 48.0,
          "work_hours_spent": {
            "spent_hours": 0.0,
            "percent_of_time": 0.0
          }
        }
      },
      "trends": null,
      "average": null,
      "total": 0.0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/duration_and_costs?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5YjY5ZTcwMi1kMTljLTRiMjktOGI2MS03ZWVhYmZlYmQ1YTkiLCJzdWIiOiI4MzAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.brhDI7M78nPYW4GW_r1XZ1vmf5AXQX5YxU83M-67UtQ"
```
## Late Scheduled Meetings


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/scheduled_late?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjNzA1ZTJiZC00Y2E0LTQ4OGEtYTllMy0yM2U5MjlhYjc5ZjUiLCJzdWIiOiI4MzIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.kmkdFyVpugpO-Fog-Ipylb-ci8iIio-gGaA8bGDy_NI
```

`GET /api/v1/reporting/user/evaluations/scheduled_late`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:29 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:29 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "13a49bbf-10d8-4b3b-a433-225e37d9b530",
    "type": "reports",
    "attributes": {
      "name": "Scheduled late",
      "starts_at": "2020-10-28T00:00:00.000Z",
      "ends_at": "2020-11-04T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
      },
      "trends": null,
      "average": 0.0,
      "total": 0.0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/scheduled_late?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjNzA1ZTJiZC00Y2E0LTQ4OGEtYTllMy0yM2U5MjlhYjc5ZjUiLCJzdWIiOiI4MzIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.kmkdFyVpugpO-Fog-Ipylb-ci8iIio-gGaA8bGDy_NI"
```
## Overtime Meeting Hours


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/overtime?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MDM4ZDgxNy1jM2Y3LTQ5Y2MtOGUxYy1jZTRkNWQ3NWRlZGMiLCJzdWIiOiI4MzQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMzAsImV4cCI6MTYwNjA2NzEzMH0.OSu2glAQehe67_PgmoeH21FubZI6w3I9PM0LM1MwMCU
```

`GET /api/v1/reporting/user/evaluations/overtime`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:29 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:29 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "5fee3d16-b267-4aed-97cb-e65146e3f569",
    "type": "reports",
    "attributes": {
      "name": "Overtime",
      "starts_at": "2020-10-28T00:00:00.000Z",
      "ends_at": "2020-11-04T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
      },
      "trends": null,
      "average": 0,
      "total": 0.0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/overtime?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MDM4ZDgxNy1jM2Y3LTQ5Y2MtOGUxYy1jZTRkNWQ3NWRlZGMiLCJzdWIiOiI4MzQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMzAsImV4cCI6MTYwNjA2NzEzMH0.OSu2glAQehe67_PgmoeH21FubZI6w3I9PM0LM1MwMCU"
```
## Wellness Block Conflicts


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/focus_block_conflict?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&amp;by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlYmY4ZDM1NS1iYzMyLTQzZWUtODFlMi05MDExZGZiODdhMWQiLCJzdWIiOiI4MzEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.tDCJqN4qN5ME6sIi_3IlbmYlxFM-cpOW4pSpdPPFnTs
```

`GET /api/v1/reporting/user/evaluations/focus_block_conflict`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-28 17:45:29 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-04 17:45:29 UTC&quot;}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |
| with_trends  | Boolean show trends |
| by_attendee_status  | Filter by attendee status |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "6b4205bf-e5a4-4ac4-ae0a-e0c9a6e78bca",
    "type": "reports",
    "attributes": {
      "name": "Focus block conflict",
      "starts_at": "2020-10-28T00:00:00.000Z",
      "ends_at": "2020-11-04T23:59:59.999Z",
      "spans_days": 8,
      "rows": {
      },
      "trends": null,
      "average": 0.0,
      "total": 0.0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/focus_block_conflict?by_period[starts_at]=2020-10-28+17%3A45%3A29+UTC&by_period[ends_at]=2020-11-04+17%3A45%3A29+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlYmY4ZDM1NS1iYzMyLTQzZWUtODFlMi05MDExZGZiODdhMWQiLCJzdWIiOiI4MzEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjksImV4cCI6MTYwNjA2NzEyOX0.tDCJqN4qN5ME6sIi_3IlbmYlxFM-cpOW4pSpdPPFnTs"
```
# Settings Labels



## List settings labels


### Request

#### Endpoint

```plaintext
GET /api/v1/settings_labels
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyM2JkODJjYy0yYmFhLTRkZTctOGEzMC0wODU4ZDQyNjYzNTEiLCJzdWIiOiI3MTEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.MWOLcesXdbGFv5SgOxFAPZhozHD3Jgcg5Gf-NURe3ik
```

`GET /api/v1/settings_labels`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "2a9275d8-6cbd-426f-899a-01fa17a5378a",
    "type": "settings_labels",
    "attributes": {
      "list": {
        "focus_block_conflict": {
          "label": "Wellness block conflict",
          "negative_label": "Wellness block conflicts",
          "positive_label": "No wellness block conflicts",
          "description": "Virtually sacred time set aside for getting work done.",
          "weight": 0.21
        },
        "meeting_conflict": {
          "label": "Meeting conflict",
          "negative_label": "Meeting conflicts",
          "positive_label": "No meeting conflicts",
          "description": "Meeting scheduled over one already accepted -- or one that the invitee created themselves.",
          "weight": 0.16
        },
        "last_minute_schedule": {
          "label": "Last minute invite",
          "negative_label": "Scheduled last minute",
          "positive_label": "Scheduled on-time",
          "description": "Hours ahead of time that a meeting must be scheduled.",
          "weight": 0.16
        },
        "compliance_deadline": {
          "label": "Deadline",
          "description": "Hours ahead of a meeting before it's considered 'not compliant'."
        },
        "non_compliance_action": {
          "label": "Action to take",
          "description": "Action when meeting requirements are not met before deadline.",
          "premium": true
        },
        "max_attendees": {
          "label": "Number of attendees",
          "negative_label": "Too many people",
          "positive_label": "Good amount of people",
          "description": "Max # of people in a meeting. Ignored for \"all hands\" and all-day meetings.",
          "weight": 0.06
        },
        "desired_duration": {
          "label": "Ideal meeting duration",
          "negative_label": "Meeting is too long",
          "positive_label": "Good meeting duration",
          "description": "Meeting length goal.",
          "weight": 0.06
        },
        "required_agenda": {
          "label": "Agenda",
          "negative_label": "Missing an agenda",
          "positive_label": "Has an agenda",
          "description": "Time-boxed items to discuss.",
          "weight": 0.21
        },
        "required_category": {
          "label": "Category",
          "negative_label": "Missing a category",
          "positive_label": "Has a category",
          "description": "Type of meeting being created.",
          "weight": null
        },
        "required_intention": {
          "label": "Intention",
          "negative_label": "Missing an intention",
          "positive_label": "Has an intention",
          "description": "The reason for meeting.",
          "weight": 0.06
        },
        "required_objectives": {
          "label": "Objectives",
          "negative_label": "Missing objective(s)",
          "positive_label": "Has objective(s)",
          "description": "Goals of the meeting.",
          "weight": 0.11
        },
        "required_prework": {
          "label": "Pre-work",
          "negative_label": "Pre-work is needed",
          "positive_label": "Pre-work is done",
          "description": "Tasks and/or associated materials to address beforehand.",
          "weight": null
        },
        "required_outcomes": {
          "label": "Outcomes",
          "negative_label": "Missing outcomes",
          "positive_label": "Has outcomes",
          "description": "Post-meeting notes with next steps.",
          "weight": null,
          "coming_soon": true
        },
        "required_role_leader": {
          "label": "Assigned leader",
          "negative_label": "Missing an assigned leader",
          "positive_label": "A leader is assigned",
          "description": "To lead the meeting.",
          "weight": null,
          "coming_soon": true
        },
        "required_role_time_keeper": {
          "label": "Assigned Time-keeper",
          "negative_label": "Missing an assigned time-keeper",
          "positive_label": "A time-keeper is assigned",
          "description": "To keep it on track.",
          "weight": null,
          "coming_soon": true
        },
        "required_role_recorder": {
          "label": "Assigned Note-taker",
          "negative_label": "Missing an assigned note-taker",
          "positive_label": "A note-taker is assigned",
          "description": "To capture parking lot items and outcomes.",
          "weight": null,
          "coming_soon": true
        },
        "required_attendee_roles": {
          "label": "Assign all roles",
          "negative_label": "Missing assigned meeting roles",
          "positive_label": "Meeting roles are assigned",
          "description": "All of the attendee roles are need to be assigned.",
          "weight": null,
          "coming_soon": true
        },
        "ignore_all_day_meetings": {
          "label": "All-day meetings",
          "description": "Do not evaluate all day meetings."
        },
        "ignore_all_hands_meetings": {
          "label": "All-hands meetings",
          "description": "Do not evaluate all hands meetings."
        }
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/settings_labels" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyM2JkODJjYy0yYmFhLTRkZTctOGEzMC0wODU4ZDQyNjYzNTEiLCJzdWIiOiI3MTEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.MWOLcesXdbGFv5SgOxFAPZhozHD3Jgcg5Gf-NURe3ik"
```
# Stripe

Stripe Subscriptions

## Create Stripe Session


### Request

#### Endpoint

```plaintext
POST /api/v1/stripe_checkout/sessions
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4ODQ3MTk5OS1iZTEwLTRiNTMtODY3OC0xMjFlMWQxOGZhYWEiLCJzdWIiOiI4MTUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.mytv7grc9oZFBnLKg-GWtms1wsXN3QxINhfPlYxwoGQ
```

`POST /api/v1/stripe_checkout/sessions`

#### Parameters


```json
{"data":{"type":"stripe_sessions","attributes":{"key":"team-400"}}}
```

None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "test_cs_1",
    "type": "stripe_sessions",
    "attributes": {
      "item": {
        "plan": "team-400",
        "quantity": 1
      },
      "status": "in_progress"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/stripe_checkout/sessions" -d '{"data":{"type":"stripe_sessions","attributes":{"key":"team-400"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4ODQ3MTk5OS1iZTEwLTRiNTMtODY3OC0xMjFlMWQxOGZhYWEiLCJzdWIiOiI4MTUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.mytv7grc9oZFBnLKg-GWtms1wsXN3QxINhfPlYxwoGQ"
```
## Delete Stripe Subscription


### Request

#### Endpoint

```plaintext
DELETE /api/v1/subscription
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmN2M2NzZjYS1lMTk2LTQyYWUtYjA2OC0zYTJhYzA5ZjBmZmIiLCJzdWIiOiI3MzQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.aymBcDIaa43rDfsFjWQ2BidW1VqshAx_NFWVGGby-zY
```

`DELETE /api/v1/subscription`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "67",
    "type": "subscriptions",
    "attributes": {
      "stripe_id": "test_su_4",
      "active": false,
      "created_at": "2020-10-28T17:45:15.738Z",
      "current_period_start": "2020-10-28T17:45:15.000Z",
      "current_period_end": "2020-11-28T17:45:15.000Z",
      "amount": 193,
      "category": "team",
      "plan": "pro",
      "product_id": "team"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/subscription" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmN2M2NzZjYS1lMTk2LTQyYWUtYjA2OC0zYTJhYzA5ZjBmZmIiLCJzdWIiOiI3MzQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.aymBcDIaa43rDfsFjWQ2BidW1VqshAx_NFWVGGby-zY"
```
## Update Stripe Session


### Request

#### Endpoint

```plaintext
PUT /api/v1/stripe_checkout/sessions
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkOWRlM2Y4Zi1kNjNkLTQzMzEtYmZhOC03MTZmM2I2YWQ3MTUiLCJzdWIiOiI4MTYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.8yBqEX3Ng6R5A0i9R8BIvM2A6Oofons0pvG_S080DmE
```

`PUT /api/v1/stripe_checkout/sessions`

#### Parameters


```json
{"data":{"type":"stripe_sessions","attributes":{"key":"team-400"}}}
```

None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "test_cs_1",
    "type": "stripe_sessions",
    "attributes": {
      "item": null,
      "status": "in_progress"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/stripe_checkout/sessions" -d '{"data":{"type":"stripe_sessions","attributes":{"key":"team-400"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkOWRlM2Y4Zi1kNjNkLTQzMzEtYmZhOC03MTZmM2I2YWQ3MTUiLCJzdWIiOiI4MTYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.8yBqEX3Ng6R5A0i9R8BIvM2A6Oofons0pvG_S080DmE"
```
## Update Stripe Subscription


### Request

#### Endpoint

```plaintext
PUT /api/v1/subscription
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjNzg0ZDQyMi03NzhmLTQ5YWMtYWVlOC0yNDE2ZTE3Mjk3OGIiLCJzdWIiOiI3MzMiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.5HxBNJGIOOu6Cr4aFoUcyycYCHWUOuI6smLV-pTmzlM
```

`PUT /api/v1/subscription`

#### Parameters


```json
{"data":{"type":"subscriptions","attributes":{"key":"pro"}}}
```

None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "66",
    "type": "subscriptions",
    "attributes": {
      "stripe_id": "test_txn_default",
      "active": true,
      "created_at": "2020-10-28T17:45:15.600Z",
      "current_period_start": "2020-10-28T17:45:15.000Z",
      "current_period_end": "2020-11-28T17:45:15.000Z",
      "amount": 193,
      "category": "team",
      "plan": "pro",
      "product_id": "team"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/subscription" -d '{"data":{"type":"subscriptions","attributes":{"key":"pro"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjNzg0ZDQyMi03NzhmLTQ5YWMtYWVlOC0yNDE2ZTE3Mjk3OGIiLCJzdWIiOiI3MzMiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.5HxBNJGIOOu6Cr4aFoUcyycYCHWUOuI6smLV-pTmzlM"
```
# Subscription



## Show subscription


### Request

#### Endpoint

```plaintext
GET /api/v1/subscription
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4YjQ3OWI1Yy0yMjlhLTRmYjUtYTI4NS0zM2M0OTVjYmMxNWQiLCJzdWIiOiI3NTciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.HWvLYP7CinjIW1xgutUUHxiAE4su5fHXdrUixFtSyY4
```

`GET /api/v1/subscription`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "68",
    "type": "subscriptions",
    "attributes": {
      "stripe_id": "tok_mastercard",
      "active": true,
      "created_at": "2020-10-28T17:45:18.817Z",
      "current_period_start": null,
      "current_period_end": null,
      "amount": 193,
      "category": "user",
      "plan": "team-193",
      "product_id": "team-400"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/subscription" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4YjQ3OWI1Yy0yMjlhLTRmYjUtYTI4NS0zM2M0OTVjYmMxNWQiLCJzdWIiOiI3NTciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.HWvLYP7CinjIW1xgutUUHxiAE4su5fHXdrUixFtSyY4"
```
# Subscription Plans



## List subscription plans


### Request

#### Endpoint

```plaintext
GET /api/v1/subscription_plans
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1YmNiMjUxYi05NjBiLTRkZjMtYjIwOC0xNDJiYjY5Yjc1N2YiLCJzdWIiOiI4MTIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.K5NHTAy9ibPiHdk_QKQKGzFrQGPol0XSkJwxXPSIEgY
```

`GET /api/v1/subscription_plans`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/subscription_plans" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1YmNiMjUxYi05NjBiLTRkZjMtYjIwOC0xNDJiYjY5Yjc1N2YiLCJzdWIiOiI4MTIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjcsImV4cCI6MTYwNjA2NzEyN30.K5NHTAy9ibPiHdk_QKQKGzFrQGPol0XSkJwxXPSIEgY"
```
# Team Invites



## Create invite


### Request

#### Endpoint

```plaintext
POST /api/v1/invites
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhOGIzY2EwOS1iNTg5LTQ2OTUtYTk5Ny1kMGQwYWJhZDAzODkiLCJzdWIiOiI4MTkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjgsImV4cCI6MTYwNjA2NzEyOH0.z7gp2hzip7SfRyeCxwnQA6AN2WdHa2zuNhNeZVmObeQ
```

`POST /api/v1/invites`

#### Parameters


```json
{"data":{"type":"agenda_item","attributes":{"email":"michale.tremblay@lebsack.biz"}}}
```


| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "12",
    "type": "invites",
    "attributes": {
      "team_id": 831,
      "user_id": 820,
      "email": "michale.tremblay@lebsack.biz",
      "created_at": "2020-10-28T17:45:28.287Z",
      "accepted_at": "2020-10-28T17:45:28.365Z"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/invites" -d '{"data":{"type":"agenda_item","attributes":{"email":"michale.tremblay@lebsack.biz"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhOGIzY2EwOS1iNTg5LTQ2OTUtYTk5Ny1kMGQwYWJhZDAzODkiLCJzdWIiOiI4MTkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjgsImV4cCI6MTYwNjA2NzEyOH0.z7gp2hzip7SfRyeCxwnQA6AN2WdHa2zuNhNeZVmObeQ"
```
## Delete invite


### Request

#### Endpoint

```plaintext
DELETE /api/v1/invites/11
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkNzBiN2ZhOS03MTM4LTRmMjEtOWU0MS1kMTM4YzM2ZWRiNjUiLCJzdWIiOiI4MTciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjgsImV4cCI6MTYwNjA2NzEyOH0.v1p411ux5WfbUpbTOtL23257d1_ZUcj39BkZ633l9Kc
```

`DELETE /api/v1/invites/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/invites/11" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkNzBiN2ZhOS03MTM4LTRmMjEtOWU0MS1kMTM4YzM2ZWRiNjUiLCJzdWIiOiI4MTciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjgsImV4cCI6MTYwNjA2NzEyOH0.v1p411ux5WfbUpbTOtL23257d1_ZUcj39BkZ633l9Kc"
```
## List invites


### Request

#### Endpoint

```plaintext
GET /api/v1/invites
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNzkxZDg0My05NjdmLTQ5ZjEtODA0ZC1lNWNlYjYxMWY4ZDgiLCJzdWIiOiI4MjEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjgsImV4cCI6MTYwNjA2NzEyOH0.-rZ6IsWzdbiBiJhsDKVDQEQRC4D2mlK8eKpjaHcUIjk
```

`GET /api/v1/invites`

#### Parameters



| Name | Description |
|:-----|:------------|
| email *required* |  email |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/invites" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNzkxZDg0My05NjdmLTQ5ZjEtODA0ZC1lNWNlYjYxMWY4ZDgiLCJzdWIiOiI4MjEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjgsImV4cCI6MTYwNjA2NzEyOH0.-rZ6IsWzdbiBiJhsDKVDQEQRC4D2mlK8eKpjaHcUIjk"
```
# Team Members



## Add membership to team


### Request

#### Endpoint

```plaintext
POST /api/v1/teams/707/members
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1YTg0MTM0Mi0xOTI0LTRjNjYtOGFiMC0yMzkzOTZhMDM4YTMiLCJzdWIiOiI2OTciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTEsImV4cCI6MTYwNjA2NzExMX0.QqYYnBX9Ih-nMsHECaiuedg4jwPBQb_9QEFoZ2sXM7w
```

`POST /api/v1/teams/:id/members`

#### Parameters


```json
{"data":{"type":"team","attributes":{"user_id":699,"role":"billing_admin"}}}
```


| Name | Description |
|:-----|:------------|
| user_id *required* |  user |
| role  | user or billing_admin |
| licensed  | boolean |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "731",
    "type": "memberships",
    "attributes": {
      "user_id": 699,
      "role": "billing_admin",
      "name": "Doctor Valkyrie II Ultra Gorilla Grodd",
      "email": "test2@test.com",
      "licensed": false,
      "profile_image": "http://boyer-ankunding.net/walton.bashirian"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/teams/707/members" -d '{"data":{"type":"team","attributes":{"user_id":699,"role":"billing_admin"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1YTg0MTM0Mi0xOTI0LTRjNjYtOGFiMC0yMzkzOTZhMDM4YTMiLCJzdWIiOiI2OTciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTEsImV4cCI6MTYwNjA2NzExMX0.QqYYnBX9Ih-nMsHECaiuedg4jwPBQb_9QEFoZ2sXM7w"
```
## Delete membership


### Request

#### Endpoint

```plaintext
DELETE /api/v1/teams/713/members/740
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MTgzNWY3Ni1mYjU4LTRlNGEtODM3Yy04N2YzOWM1NTMyNDIiLCJzdWIiOiI3MDQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTEsImV4cCI6MTYwNjA2NzExMX0.7xoZW8B6HMyB7PfCh1BYrCO5FXRKYo9qISboAG0pL3s
```

`DELETE /api/v1/teams/:id/members/:membership_id`

#### Parameters



| Name | Description |
|:-----|:------------|
| user_id *required* |  user |
| role  | user or billing_admin |
| licensed  | boolean |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/teams/713/members/740" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MTgzNWY3Ni1mYjU4LTRlNGEtODM3Yy04N2YzOWM1NTMyNDIiLCJzdWIiOiI3MDQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTEsImV4cCI6MTYwNjA2NzExMX0.7xoZW8B6HMyB7PfCh1BYrCO5FXRKYo9qISboAG0pL3s"
```
## List team memberships


### Request

#### Endpoint

```plaintext
GET /api/v1/teams/711/members
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3ZTU1MGFmNi00Yjc4LTRkMWQtOTFhMy00MDYzMGE0NGVlODMiLCJzdWIiOiI3MDIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTEsImV4cCI6MTYwNjA2NzExMX0.a-L5EwrychvjaD54BBRIFRdN11rG2rIHigfDstgQuVI
```

`GET /api/v1/teams/:id/members`

#### Parameters



| Name | Description |
|:-----|:------------|
| user_id *required* |  user |
| role  | user or billing_admin |
| licensed  | boolean |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "735",
      "type": "memberships",
      "attributes": {
        "user_id": 702,
        "role": "billing_admin",
        "name": "Hancock Strike Lizard",
        "email": "garret@greenfelder.net",
        "licensed": true,
        "profile_image": "http://will.co/laurence"
      }
    },
    {
      "id": "737",
      "type": "memberships",
      "attributes": {
        "user_id": 703,
        "role": "billing_admin",
        "name": "Sage Claw Dark Sabretooth the Fated",
        "email": "test1@test.com",
        "licensed": true,
        "profile_image": "http://mills.org/jordan_ruecker"
      }
    }
  ],
  "meta": {
    "member_count": 2,
    "licensed_member_count": 2
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/teams/711/members" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3ZTU1MGFmNi00Yjc4LTRkMWQtOTFhMy00MDYzMGE0NGVlODMiLCJzdWIiOiI3MDIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTEsImV4cCI6MTYwNjA2NzExMX0.a-L5EwrychvjaD54BBRIFRdN11rG2rIHigfDstgQuVI"
```
## Update membership


### Request

#### Endpoint

```plaintext
PUT /api/v1/teams/709/members/734
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyZTNkZTE0YS1lZTliLTRkMmUtOTE1ZC03ODcyNzA4ZTc4ODIiLCJzdWIiOiI3MDAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTEsImV4cCI6MTYwNjA2NzExMX0.lGlcyAJFS-i7ETfA7et6vtPzAfMF8MbORtn2SMe6rgw
```

`PUT /api/v1/teams/:id/members/:membership_id`

#### Parameters


```json
{"data":{"type":"team","attributes":{"role":"billing_admin","licensed":true}}}
```


| Name | Description |
|:-----|:------------|
| user_id *required* |  user |
| role  | user or billing_admin |
| licensed  | boolean |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "734",
    "type": "memberships",
    "attributes": {
      "user_id": 701,
      "role": "billing_admin",
      "name": "Beak Spirit Supah Bloodhawk",
      "email": "test1@test.com",
      "licensed": true,
      "profile_image": "http://schulist.io/darlena"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/teams/709/members/734" -d '{"data":{"type":"team","attributes":{"role":"billing_admin","licensed":true}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyZTNkZTE0YS1lZTliLTRkMmUtOTE1ZC03ODcyNzA4ZTc4ODIiLCJzdWIiOiI3MDAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTEsImV4cCI6MTYwNjA2NzExMX0.lGlcyAJFS-i7ETfA7et6vtPzAfMF8MbORtn2SMe6rgw"
```
# Teams



## List teams


### Request

#### Endpoint

```plaintext
GET /api/v1/teams
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5NmQ4OGI4Mi05ZGI2LTQwZjYtOWMyNy1jYmQ2ZWNhNjM3YTkiLCJzdWIiOiI3ODgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjMsImV4cCI6MTYwNjA2NzEyM30.UJEJ-tKZpIY2PS7SD-5OFrYlzSZrTDBzSjQieY_48Jo
```

`GET /api/v1/teams`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "798",
      "type": "teams",
      "attributes": {
        "name": "rowe-kuvalis",
        "image": null,
        "domain": "rowe-kuvalis.info",
        "license_by": "domain",
        "current_user_membership": {
          "id": 823,
          "user_id": 788,
          "created_at": "2020-10-28T17:45:23.596Z",
          "updated_at": "2020-10-28T17:45:23.596Z",
          "role": "billing_admin",
          "team_id": 798,
          "licensed": true
        }
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/teams" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5NmQ4OGI4Mi05ZGI2LTQwZjYtOWMyNy1jYmQ2ZWNhNjM3YTkiLCJzdWIiOiI3ODgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjMsImV4cCI6MTYwNjA2NzEyM30.UJEJ-tKZpIY2PS7SD-5OFrYlzSZrTDBzSjQieY_48Jo"
```
## Show team


### Request

#### Endpoint

```plaintext
GET /api/v1/teams/800
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2YjQ0M2U3Yy01NGI0LTQ3NDQtOWEzOS1lZjI4OTY5Y2IxOTEiLCJzdWIiOiI3OTAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjQsImV4cCI6MTYwNjA2NzEyNH0.iJ_cImbptbdN0zp3pjd3xV3ANuPbRP-nhqoSpwzyf1s
```

`GET /api/v1/teams/:id`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "800",
    "type": "teams",
    "attributes": {
      "name": "casper-cummings",
      "image": null,
      "domain": "casper-cummings.io",
      "license_by": "domain",
      "current_user_membership": {
        "id": 825,
        "user_id": 790,
        "created_at": "2020-10-28T17:45:23.975Z",
        "updated_at": "2020-10-28T17:45:23.975Z",
        "role": "billing_admin",
        "team_id": 800,
        "licensed": true
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/teams/800" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2YjQ0M2U3Yy01NGI0LTQ3NDQtOWEzOS1lZjI4OTY5Y2IxOTEiLCJzdWIiOiI3OTAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjQsImV4cCI6MTYwNjA2NzEyNH0.iJ_cImbptbdN0zp3pjd3xV3ANuPbRP-nhqoSpwzyf1s"
```
## Update team


### Request

#### Endpoint

```plaintext
PUT /api/v1/teams/799
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwM2IxOTQyMi0xMzI1LTQ1ZWItOWE0ZS1lZGM3Yjg3ODllYjAiLCJzdWIiOiI3ODkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjMsImV4cCI6MTYwNjA2NzEyM30.iTBUEorC_OwD-aKJovjBb2jBFR3e3tEDg1EgVJehiyg
```

`PUT /api/v1/teams/:id`

#### Parameters


```json
{"data":{"type":"team","attributes":{"required_category":true,"required_agenda":true,"license_by":"invite","annual_salary":220000}}}
```


| Name | Description |
|:-----|:------------|
| evaluation_setting  |  evaluation setting |
| action_setting  |  action setting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "799",
    "type": "teams",
    "attributes": {
      "name": "hoeger-aufderhar",
      "image": null,
      "domain": "hoeger-aufderhar.co",
      "license_by": "invite",
      "current_user_membership": {
        "id": 824,
        "user_id": 789,
        "created_at": "2020-10-28T17:45:23.774Z",
        "updated_at": "2020-10-28T17:45:23.774Z",
        "role": "billing_admin",
        "team_id": 799,
        "licensed": true
      }
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/teams/799" -d '{"data":{"type":"team","attributes":{"required_category":true,"required_agenda":true,"license_by":"invite","annual_salary":220000}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwM2IxOTQyMi0xMzI1LTQ1ZWItOWE0ZS1lZGM3Yjg3ODllYjAiLCJzdWIiOiI3ODkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMjMsImV4cCI6MTYwNjA2NzEyM30.iTBUEorC_OwD-aKJovjBb2jBFR3e3tEDg1EgVJehiyg"
```
# Tips



## Clear all tips for user


### Request

#### Endpoint

```plaintext
DELETE /api/v1/tips/all
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMTJiZjMwOS1kZmI2LTQ2NmYtYWU3NC0zZDQ1ZjkyMzIzNDYiLCJzdWIiOiI3MDYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTEsImV4cCI6MTYwNjA2NzExMX0.04mS6Cr47wGCZ3YEd4TFVfWEpubPzYox_d9iB4QlyQ4
```

`DELETE /api/v1/tips/all`

#### Parameters


None known.


### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/tips/all" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMTJiZjMwOS1kZmI2LTQ2NmYtYWU3NC0zZDQ1ZjkyMzIzNDYiLCJzdWIiOiI3MDYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTEsImV4cCI6MTYwNjA2NzExMX0.04mS6Cr47wGCZ3YEd4TFVfWEpubPzYox_d9iB4QlyQ4"
```
## Flag tip as seen for user


### Request

#### Endpoint

```plaintext
PUT /api/v1/tips/5
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MTdkNjcwZi01ZDgwLTRjNzUtYmNiNi04YWE4N2UyMTg4MTQiLCJzdWIiOiI3MDciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTEsImV4cCI6MTYwNjA2NzExMX0.iXI-PeO1s5ruG_pFmrWmMhz6yJ3BLBJf8vnIQX4vfb8
```

`PUT /api/v1/tips/:id`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "5",
    "type": "tip",
    "attributes": {
      "title": "Balance",
      "description": "Featuring your meeting preferences that are pre-optimized based on research from meeting experts.",
      "tag": "view-balance",
      "seen_at": "2020-10-28T17:45:11.925Z"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/tips/5" -d '' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MTdkNjcwZi01ZDgwLTRjNzUtYmNiNi04YWE4N2UyMTg4MTQiLCJzdWIiOiI3MDciLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTEsImV4cCI6MTYwNjA2NzExMX0.iXI-PeO1s5ruG_pFmrWmMhz6yJ3BLBJf8vnIQX4vfb8"
```
## List tips for user


### Request

#### Endpoint

```plaintext
GET /api/v1/tips
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4YjMyMTNkOS01OWM4LTQ3ZjAtYjU3Ny0xMTE2ZWE2MTRkZjIiLCJzdWIiOiI3MDgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.efmqEZ3keb-RWWF9dtyGphmfvg3wzHB38SIMitl3XxM
```

`GET /api/v1/tips`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [
    {
      "id": "1",
      "type": "tip",
      "attributes": {
        "title": "Add info from your calendar!",
        "description": "Agenda items and objectives can be added from the description in your meeting invite in Google or Outlook. We will organize it nicely for you!",
        "tag": "agenda-parser",
        "seen_at": null
      }
    },
    {
      "id": "2",
      "type": "tip",
      "attributes": {
        "title": "Auto-Balance",
        "description": "By default, MeetWell automatically interacts with meeting invites that stray from your preferences. You’ll receive an email before any action is taken. This is where the REAL (time-saving) magic happens.",
        "tag": "non-compliance-action",
        "seen_at": null
      }
    },
    {
      "id": "3",
      "type": "tip",
      "attributes": {
        "title": "Review",
        "description": "This view allows you to monitor yours and/or your team's overall meeting health and behaviors during any stretch of time.",
        "tag": "view-review",
        "seen_at": null
      }
    },
    {
      "id": "4",
      "type": "tip",
      "attributes": {
        "title": "Plan",
        "description": "This view features your week at a glance, and more!",
        "tag": "view-plan",
        "seen_at": null
      }
    },
    {
      "id": "5",
      "type": "tip",
      "attributes": {
        "title": "Balance",
        "description": "Featuring your meeting preferences that are pre-optimized based on research from meeting experts.",
        "tag": "view-balance",
        "seen_at": null
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/tips" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4YjMyMTNkOS01OWM4LTQ3ZjAtYjU3Ny0xMTE2ZWE2MTRkZjIiLCJzdWIiOiI3MDgiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTIsImV4cCI6MTYwNjA2NzExMn0.efmqEZ3keb-RWWF9dtyGphmfvg3wzHB38SIMitl3XxM"
```
# User Settings



## Show user settings


### Request

#### Endpoint

```plaintext
GET /api/v1/users/settings
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0ODIzODljYi00ZDFjLTQzMDktYWFmOC1jM2FkNzc2ZGJmYTMiLCJzdWIiOiI3NDkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTcsImV4cCI6MTYwNjA2NzExN30.EBtbXDj9D5n3zxDL4SsKowGVa0dnGe3TnDAXWr_lQlE
```

`GET /api/v1/users/settings`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "749",
    "type": "user_settings",
    "attributes": {
      "action_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "non_compliance_action": "remind",
        "domains_whitelist": "bergstrom.org",
        "last_minute_schedule": 6,
        "compliance_deadline": 6,
        "max_attendees": 12,
        "desired_duration": 90,
        "required_agenda": true,
        "required_category": false,
        "required_intention": false,
        "required_objectives": false,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false
      },
      "default_action_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "non_compliance_action": "remind",
        "domains_whitelist": null,
        "last_minute_schedule": 6,
        "compliance_deadline": 6,
        "max_attendees": 12,
        "desired_duration": 90,
        "required_agenda": true,
        "required_category": false,
        "required_intention": false,
        "required_objectives": false,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false
      },
      "evaluation_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "last_minute_schedule": 24,
        "max_attendees": 8,
        "desired_duration": 45,
        "required_agenda": true,
        "required_category": false,
        "required_intention": true,
        "required_objectives": true,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false,
        "ignore_all_day_meetings": true,
        "ignore_all_hands_meetings": true,
        "annual_salary": 75000
      },
      "default_evaluation_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "last_minute_schedule": 24,
        "max_attendees": 8,
        "desired_duration": 45,
        "required_agenda": true,
        "required_category": false,
        "required_intention": true,
        "required_objectives": true,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false,
        "ignore_all_day_meetings": true,
        "ignore_all_hands_meetings": true,
        "annual_salary": 75000
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/users/settings" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0ODIzODljYi00ZDFjLTQzMDktYWFmOC1jM2FkNzc2ZGJmYTMiLCJzdWIiOiI3NDkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTcsImV4cCI6MTYwNjA2NzExN30.EBtbXDj9D5n3zxDL4SsKowGVa0dnGe3TnDAXWr_lQlE"
```
## Update user settings


### Request

#### Endpoint

```plaintext
PUT /api/v1/users/settings
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYjViZjhmMC0xYjUyLTQyMzgtYTM0NC0xYTMzYjIzNzY2MDciLCJzdWIiOiI3NTAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTcsImV4cCI6MTYwNjA2NzExN30.byM1UXf6aU1nGyzSVKk-OjzUIHrQhC1D4tRpIYFjja8
```

`PUT /api/v1/users/settings`

#### Parameters


```json
{"data":{"type":"team","attributes":{"action_settings":{"required_agenda":false,"desired_duration":60,"last_minute_schedule":6},"evaluation_settings":{"max_attendees":8}}}}
```


| Name | Description |
|:-----|:------------|
| evaluation_setting  |  evaluation setting |
| action_setting  |  action setting |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "750",
    "type": "user_settings",
    "attributes": {
      "action_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "non_compliance_action": "remind",
        "domains_whitelist": "hintz-considine.com",
        "last_minute_schedule": 6,
        "compliance_deadline": 6,
        "max_attendees": 12,
        "desired_duration": 60,
        "required_agenda": false,
        "required_category": false,
        "required_intention": false,
        "required_objectives": false,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false
      },
      "default_action_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "non_compliance_action": "remind",
        "domains_whitelist": null,
        "last_minute_schedule": 6,
        "compliance_deadline": 6,
        "max_attendees": 12,
        "desired_duration": 90,
        "required_agenda": true,
        "required_category": false,
        "required_intention": false,
        "required_objectives": false,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false
      },
      "evaluation_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "last_minute_schedule": 24,
        "max_attendees": 8,
        "desired_duration": 45,
        "required_agenda": true,
        "required_category": false,
        "required_intention": true,
        "required_objectives": true,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false,
        "ignore_all_day_meetings": true,
        "ignore_all_hands_meetings": true,
        "annual_salary": 75000
      },
      "default_evaluation_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "last_minute_schedule": 24,
        "max_attendees": 8,
        "desired_duration": 45,
        "required_agenda": true,
        "required_category": false,
        "required_intention": true,
        "required_objectives": true,
        "required_prework": false,
        "required_outcomes": false,
        "required_role_leader": false,
        "required_role_time_keeper": false,
        "required_role_recorder": false,
        "required_attendee_roles": false,
        "ignore_all_day_meetings": true,
        "ignore_all_hands_meetings": true,
        "annual_salary": 75000
      }
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/users/settings" -d '{"data":{"type":"team","attributes":{"action_settings":{"required_agenda":false,"desired_duration":60,"last_minute_schedule":6},"evaluation_settings":{"max_attendees":8}}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYjViZjhmMC0xYjUyLTQyMzgtYTM0NC0xYTMzYjIzNzY2MDciLCJzdWIiOiI3NTAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTcsImV4cCI6MTYwNjA2NzExN30.byM1UXf6aU1nGyzSVKk-OjzUIHrQhC1D4tRpIYFjja8"
```
# Users

Update user attributes or evaluation settings

## Delete user account and all associated data


### Request

#### Endpoint

```plaintext
DELETE /api/v1/users
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwYWQxMWZkZC05ZmQzLTRjNWQtYWViNy04Y2U4Y2U4MTlmNGIiLCJzdWIiOiI3MzAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.SAf_ZWTmHmHky8dQ3lQgk-PFPHHSTj-nC-cH8qEf_Vc
```

`DELETE /api/v1/users`

#### Parameters


None known.


### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/users" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwYWQxMWZkZC05ZmQzLTRjNWQtYWViNy04Y2U4Y2U4MTlmNGIiLCJzdWIiOiI3MzAiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.SAf_ZWTmHmHky8dQ3lQgk-PFPHHSTj-nC-cH8qEf_Vc"
```
## Show user


### Request

#### Endpoint

```plaintext
GET /api/v1/users
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4M2NiNTIyNi01MDZiLTQyMGUtOGM5MC0zOTU4ZTQzYzM3ZjEiLCJzdWIiOiI3MzEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.zZcW_VdjdwQcE-72IR3gp81COeI86S_jEIAYlZAgHW0
```

`GET /api/v1/users`

#### Parameters


None known.


### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "731",
    "type": "users",
    "attributes": {
      "email": "guillermo_dooley@weissnat.net",
      "domain": "weissnat.net",
      "first_name": "Shatterstar",
      "last_name": "Green Darkside",
      "profile_image": "http://gutmann-mayer.net/tatiana",
      "time_zone": "UTC",
      "onboarded": false,
      "identity_providers": [

      ],
      "subscription_plan": null,
      "daily_report_card_events": true,
      "company": {
        "id": 740,
        "name": "weissnat",
        "license_by": "domain",
        "roles": [
          "billing_admin"
        ]
      },
      "organizer_blacklist": "",
      "domain_whitelist": "weissnat.net",
      "communication_prefs": {
        "all_communications": "pre_and_post",
        "email_tips": true,
        "email_weekly_reports": true,
        "email_reminders": "pre_and_post"
      },
      "goal_ids": [

      ]
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/users" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4M2NiNTIyNi01MDZiLTQyMGUtOGM5MC0zOTU4ZTQzYzM3ZjEiLCJzdWIiOiI3MzEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.zZcW_VdjdwQcE-72IR3gp81COeI86S_jEIAYlZAgHW0"
```
## Update user


### Request

#### Endpoint

```plaintext
PUT /api/v1/users
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5NDljYjQyMi0yMmRmLTQ2YjgtOWYwOS0yNDIxYTRhMDE0MTIiLCJzdWIiOiI3MjkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.P6rc3BF7M4maxvkrqv0nc4-x8qoaYbnUKh79y7Umyqw
```

`PUT /api/v1/users`

#### Parameters


```json
{"communication_prefs":{"email_reminders":"pre_and_post","all_communications":true,"email_tips":true,"email_weekly_reports":true},"data":{"type":"team","attributes":{"required_category":true,"required_agenda":true,"annual_salary":220000}}}
```


| Name | Description |
|:-----|:------------|
| evaluation_setting  |  evaluation setting |
| action_setting  |  action setting |
| communication_prefs  |  communication prefs |
| communications_prefs[all_communications]  | True value sets all prefs to true |
| communications_prefs[email_tips]  | Ex: onboarding emails |
| communications_prefs[email_reminders]  | no_email, pre_and_post, pre_action, post_action |
| communications_prefs[email_weekly_reports]  | Communications prefs email weekly reports |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "729",
    "type": "users",
    "attributes": {
      "email": "drew_wolf@bashirian-roob.com",
      "domain": "bashirian-roob.com",
      "first_name": "Falcon",
      "last_name": "Cyborg Maxima",
      "profile_image": "http://kshlerin.net/nestor",
      "time_zone": "UTC",
      "onboarded": false,
      "identity_providers": [

      ],
      "subscription_plan": null,
      "daily_report_card_events": true,
      "company": {
        "id": 738,
        "name": "bashirian-roob",
        "license_by": "domain",
        "roles": [
          "billing_admin"
        ]
      },
      "organizer_blacklist": "",
      "domain_whitelist": "bashirian-roob.com",
      "communication_prefs": {
        "all_communications": "pre_and_post",
        "email_tips": true,
        "email_weekly_reports": true,
        "email_reminders": "pre_and_post"
      },
      "goal_ids": [

      ]
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/users" -d '{"communication_prefs":{"email_reminders":"pre_and_post","all_communications":true,"email_tips":true,"email_weekly_reports":true},"data":{"type":"team","attributes":{"required_category":true,"required_agenda":true,"annual_salary":220000}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5NDljYjQyMi0yMmRmLTQ2YjgtOWYwOS0yNDIxYTRhMDE0MTIiLCJzdWIiOiI3MjkiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTUsImV4cCI6MTYwNjA2NzExNX0.P6rc3BF7M4maxvkrqv0nc4-x8qoaYbnUKh79y7Umyqw"
```
# Wellness Blocks



## Create focus block


### Request

#### Endpoint

```plaintext
POST /api/v1/focus_blocks
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiMTVhMjc4NS1mZjQ5LTRjZDktODUwMC01ZmE3M2RlZmU5MTQiLCJzdWIiOiI3NTEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTcsImV4cCI6MTYwNjA2NzExN30.iUSO304-yHVlJo3MjU6flJIxYE-9GfuUXkOiec1SiZc
```

`POST /api/v1/focus_blocks`

#### Parameters


```json
{"data":{"type":"focus_block","attributes":{"label":"Coding MeetWell","calendar_id":778,"rrule":"DTSTART;TZID=PST:20191228T140357\nRRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA","starts_at":"2019-12-28 22:03:57 UTC","ends_at":"2019-12-28 23:03:57 UTC"}}}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
201 Created
```


```json
{
  "data": {
    "id": "37",
    "type": "focus_blocks",
    "attributes": {
      "label": "Coding MeetWell",
      "category": "focus",
      "calendar_id": 778,
      "recurring_meeting_uuid": null,
      "duration": 3600,
      "starts_at": "2020-10-26T22:03:00.000Z",
      "ends_at": "2020-10-26T23:03:00.000Z",
      "rrule": "RRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA",
      "recurring": true
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/focus_blocks" -d '{"data":{"type":"focus_block","attributes":{"label":"Coding MeetWell","calendar_id":778,"rrule":"DTSTART;TZID=PST:20191228T140357\nRRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA","starts_at":"2019-12-28 22:03:57 UTC","ends_at":"2019-12-28 23:03:57 UTC"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiMTVhMjc4NS1mZjQ5LTRjZDktODUwMC01ZmE3M2RlZmU5MTQiLCJzdWIiOiI3NTEiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTcsImV4cCI6MTYwNjA2NzExN30.iUSO304-yHVlJo3MjU6flJIxYE-9GfuUXkOiec1SiZc"
```
## Delete wellness block


### Request

#### Endpoint

```plaintext
DELETE /api/v1/focus_blocks/39
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2NzY2ODdiZS1jZGQ1LTQ0YTctYmJiMy00ZTliNzg4MGE0NDgiLCJzdWIiOiI3NTUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.bg9TjkEFqRsUeX0hRzoeTTTB9NdYt4i5hcfuG_NH4EU
```

`DELETE /api/v1/focus_blocks/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/focus_blocks/39" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2NzY2ODdiZS1jZGQ1LTQ0YTctYmJiMy00ZTliNzg4MGE0NDgiLCJzdWIiOiI3NTUiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.bg9TjkEFqRsUeX0hRzoeTTTB9NdYt4i5hcfuG_NH4EU"
```
## List maybe wellness blocks


### Request

#### Endpoint

```plaintext
GET /api/v1/focus_blocks/maybe
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2Njc3NzIyZS1hNGI4LTRjYTUtOGU3Ny01NjJiYWJlMzEzZTAiLCJzdWIiOiI3NTIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.tB7yOIGISqujHmya2n2joZqua9W7vSPh9URM-11aFFQ
```

`GET /api/v1/focus_blocks/maybe`

#### Parameters



| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/focus_blocks/maybe" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2Njc3NzIyZS1hNGI4LTRjYTUtOGU3Ny01NjJiYWJlMzEzZTAiLCJzdWIiOiI3NTIiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.tB7yOIGISqujHmya2n2joZqua9W7vSPh9URM-11aFFQ"
```
## List wellness blocks


### Request

#### Endpoint

```plaintext
GET /api/v1/focus_blocks
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkOGFhZjkyMC1jN2YzLTRhNzQtODJjYS1iMGU5ODVhYmY3ODEiLCJzdWIiOiI3NTQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.8GWnkAqFF4TN_VV4tAo4Q-qUo3N_zZYPFARh_vyFHj4
```

`GET /api/v1/focus_blocks`

#### Parameters



| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": [

  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/focus_blocks" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkOGFhZjkyMC1jN2YzLTRhNzQtODJjYS1iMGU5ODVhYmY3ODEiLCJzdWIiOiI3NTQiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.8GWnkAqFF4TN_VV4tAo4Q-qUo3N_zZYPFARh_vyFHj4"
```
## Show wellness blocks


### Request

#### Endpoint

```plaintext
GET /api/v1/focus_blocks/38
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2ZGFhNWE2MC0wN2MyLTQ5ZTctODBiMy1kYjQxMWI2MDJmNjMiLCJzdWIiOiI3NTMiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.IkLaLty4f2OP1Gg57hvp1xNhlEQeXi0Z5LLFGOKcoPM
```

`GET /api/v1/focus_blocks/:id`

#### Parameters



| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
200 OK
```


```json
{
  "data": {
    "id": "38",
    "type": "focus_blocks",
    "attributes": {
      "label": "test",
      "category": "focus",
      "calendar_id": 780,
      "recurring_meeting_uuid": "foo",
      "duration": 3600,
      "starts_at": "2020-10-28T17:45:00.000Z",
      "ends_at": "2020-10-28T18:45:00.000Z",
      "rrule": "RRULE:FREQ=DAILY",
      "recurring": true
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/focus_blocks/38" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2ZGFhNWE2MC0wN2MyLTQ5ZTctODBiMy1kYjQxMWI2MDJmNjMiLCJzdWIiOiI3NTMiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.IkLaLty4f2OP1Gg57hvp1xNhlEQeXi0Z5LLFGOKcoPM"
```
## Update wellness block


### Request

#### Endpoint

```plaintext
PUT /api/v1/focus_blocks/40
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlNTFhYzk3Mi00ZGE1LTQwODItOWRhMS1kYTBmMzMxOThmNGMiLCJzdWIiOiI3NTYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.vjb_b43lgtwhIdmxvb3QvDnquCe2981WpSNFM99iCo0
```

`PUT /api/v1/focus_blocks/:id`

#### Parameters


```json
{"data":{"type":"focus_block","attributes":{"label":"test","rrule":"DTSTART;TZID=PST:20191228T140357\nRRULE:FREQ=WEEKLY;BYDAY=FR,SA","duration":3600}}}
```


| Name | Description |
|:-----|:------------|
| by_period  |  by period |
| by_period[starts_at]  | Filter by meeting start date |
| by_period[ends_at]  | Filter by meeting end date |



### Response

```plaintext
Content-Type: application/vnd.api+json; charset=utf-8
202 Accepted
```


```json
{
  "data": {
    "id": "40",
    "type": "focus_blocks",
    "attributes": {
      "label": "test",
      "category": "focus",
      "calendar_id": 783,
      "recurring_meeting_uuid": "foo",
      "duration": 3600,
      "starts_at": "2020-10-23T17:45:00.000Z",
      "ends_at": "2020-10-23T18:45:00.000Z",
      "rrule": "RRULE:FREQ=WEEKLY;BYDAY=FR,SA",
      "recurring": true
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/focus_blocks/40" -d '{"data":{"type":"focus_block","attributes":{"label":"test","rrule":"DTSTART;TZID=PST:20191228T140357\nRRULE:FREQ=WEEKLY;BYDAY=FR,SA","duration":3600}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlNTFhYzk3Mi00ZGE1LTQwODItOWRhMS1kYTBmMzMxOThmNGMiLCJzdWIiOiI3NTYiLCJzY3AiOiJ1c2VyIiwiYXVkIjpudWxsLCJpYXQiOjE2MDM5MDcxMTgsImV4cCI6MTYwNjA2NzExOH0.vjb_b43lgtwhIdmxvb3QvDnquCe2981WpSNFM99iCo0"
```
