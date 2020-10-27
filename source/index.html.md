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
POST /api/v1/meetings/5518/action_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1NTgxZDJlMS1kMTIxLTRlZjEtOTRlYi02MDYwZDM5YzdmMjgiLCJzdWIiOiIxMjI5MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NCwiZXhwIjoxNjA1ODA0OTY0fQ.3RpyQIyIJjQmg_ZWEpKZdDC_lmqrEGzLLQUFY9EOddk
```

`POST /api/v1/meetings/:meeting_id/action_items`

#### Parameters


```json
{"data":{"type":"action_item","attributes":{"description":"Discuss reticulating the splines.","owner_id":12290,"creator_id":12290,"category":"action_item","position":3,"due_by":"2020-10-26T16:56:04.200Z"}}}
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
    "id": "243",
    "type": "action_items",
    "attributes": {
      "id": 243,
      "category": "action_item",
      "owner_name": "Violet Dragon Raven Strike",
      "owner_id": 12290,
      "description": "Discuss reticulating the splines.",
      "creator_id": 12290,
      "due_by": "2020-10-26T16:56:04.200Z",
      "position": 3,
      "creator_name": "Violet Dragon Raven Strike"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/5518/action_items" -d '{"data":{"type":"action_item","attributes":{"description":"Discuss reticulating the splines.","owner_id":12290,"creator_id":12290,"category":"action_item","position":3,"due_by":"2020-10-26T16:56:04.200Z"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1NTgxZDJlMS1kMTIxLTRlZjEtOTRlYi02MDYwZDM5YzdmMjgiLCJzdWIiOiIxMjI5MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NCwiZXhwIjoxNjA1ODA0OTY0fQ.3RpyQIyIJjQmg_ZWEpKZdDC_lmqrEGzLLQUFY9EOddk"
```
## Delete action item


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/5514/action_items/240
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmOTgxOTJmNi1iNzA2LTQyNGYtOThhNS02NThlNTc1MjA3NzYiLCJzdWIiOiIxMjI4MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MywiZXhwIjoxNjA1ODA0OTYzfQ.S4Elb-me5x8eW8J4NGATRd6vCiLXB2L1rAGby-z9Xgo
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
curl "http://localhost:3000/api/v1/meetings/5514/action_items/240" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmOTgxOTJmNi1iNzA2LTQyNGYtOThhNS02NThlNTc1MjA3NzYiLCJzdWIiOiIxMjI4MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MywiZXhwIjoxNjA1ODA0OTYzfQ.S4Elb-me5x8eW8J4NGATRd6vCiLXB2L1rAGby-z9Xgo"
```
## List action items


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/5515/action_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1MjNjMjAyZS05N2M3LTQ1ZGMtOTRkYS04MjQ1NTgzY2M2MTciLCJzdWIiOiIxMjI4MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MywiZXhwIjoxNjA1ODA0OTYzfQ.wteKfwdnbzwZsaQGW3NU5Q4IG8ZwwHMBE7L_h_ezvxs
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
curl -g "http://localhost:3000/api/v1/meetings/5515/action_items" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1MjNjMjAyZS05N2M3LTQ1ZGMtOTRkYS04MjQ1NTgzY2M2MTciLCJzdWIiOiIxMjI4MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MywiZXhwIjoxNjA1ODA0OTYzfQ.wteKfwdnbzwZsaQGW3NU5Q4IG8ZwwHMBE7L_h_ezvxs"
```
## Show action item


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/5516/action_items/241
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2Y2MwODM4YS1jODE1LTQ3MzYtYTJiZi00YWI1MDYyNzU2OTQiLCJzdWIiOiIxMjI4NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MywiZXhwIjoxNjA1ODA0OTYzfQ.FYHlVrlhCwkIwQTU4oP2mdx4zXzz682C7JG_DF5fqYo
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
    "id": "241",
    "type": "action_items",
    "attributes": {
      "id": 241,
      "category": "action_item",
      "owner_name": "Bat Atom",
      "owner_id": 12285,
      "description": "Ugh ennui godard tofu street narwhal bushwick hoodie.",
      "creator_id": 12286,
      "due_by": "2020-10-27T16:56:03.700Z",
      "position": 1,
      "creator_name": "Aztar Illustrious Brainiac"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/5516/action_items/241" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2Y2MwODM4YS1jODE1LTQ3MzYtYTJiZi00YWI1MDYyNzU2OTQiLCJzdWIiOiIxMjI4NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MywiZXhwIjoxNjA1ODA0OTYzfQ.FYHlVrlhCwkIwQTU4oP2mdx4zXzz682C7JG_DF5fqYo"
```
## Update action item


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/5517/action_items/242
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwYjM2YzMzOC1lM2I3LTQ5ZWMtODQ2NC0wMDFhZDc0YjkxMWIiLCJzdWIiOiIxMjI4NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NCwiZXhwIjoxNjA1ODA0OTY0fQ.XJp8X9CLReCgi4wwhd9EOYP49AzkqLmnhEk6fTSVjmE
```

`PUT /api/v1/meetings/:meeting_id/action_items/:id`

#### Parameters


```json
{"data":{"type":"action_item","attributes":{"description":"Talk.","owner_id":12287,"creator_id":12287,"category":"action_item","position":2,"due_by":"2020-10-26T16:56:03.827Z"}}}
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
    "id": "242",
    "type": "action_items",
    "attributes": {
      "id": 242,
      "category": "action_item",
      "owner_name": "General Wolverine Ivy The Cloak",
      "owner_id": 12287,
      "description": "Talk.",
      "creator_id": 12287,
      "due_by": "2020-10-26T16:56:03.827Z",
      "position": 2,
      "creator_name": "General Wolverine Ivy The Cloak"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/5517/action_items/242" -d '{"data":{"type":"action_item","attributes":{"description":"Talk.","owner_id":12287,"creator_id":12287,"category":"action_item","position":2,"due_by":"2020-10-26T16:56:03.827Z"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwYjM2YzMzOC1lM2I3LTQ5ZWMtODQ2NC0wMDFhZDc0YjkxMWIiLCJzdWIiOiIxMjI4NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NCwiZXhwIjoxNjA1ODA0OTY0fQ.XJp8X9CLReCgi4wwhd9EOYP49AzkqLmnhEk6fTSVjmE"
```
# Actions



## List future actions


### Request

#### Endpoint

```plaintext
GET /api/v1/future_actions?by_period[starts_at]=2020-10-25+16%3A56%3A01+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A01+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjMDI5MjVmYi0xYzY0LTRmNzYtOGY5My1mZWUxNThjOTEwMWMiLCJzdWIiOiIxMjI3NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MiwiZXhwIjoxNjA1ODA0OTYyfQ.GdEIOJ3oDTMitXlgla_P__VqzuybwCOwtm7A2rlybqU
```

`GET /api/v1/future_actions`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:01 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:01 UTC&quot;}
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
curl -g "http://localhost:3000/api/v1/future_actions?by_period[starts_at]=2020-10-25+16%3A56%3A01+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A01+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjMDI5MjVmYi0xYzY0LTRmNzYtOGY5My1mZWUxNThjOTEwMWMiLCJzdWIiOiIxMjI3NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MiwiZXhwIjoxNjA1ODA0OTYyfQ.GdEIOJ3oDTMitXlgla_P__VqzuybwCOwtm7A2rlybqU"
```
## List past actions


### Request

#### Endpoint

```plaintext
GET /api/v1/past_actions?by_period[starts_at]=2020-10-25+16%3A56%3A05+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A05+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0NmZlZGZkNC1mYWEyLTQ5ZjktOTE2Ni0wYjViNmI2ODc0MjkiLCJzdWIiOiIxMjMwMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NSwiZXhwIjoxNjA1ODA0OTY1fQ.iAl77Yl-6OLd2rzWmQyVqz3lnxRhkp2TVZj7dMZjQK8
```

`GET /api/v1/past_actions`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:05 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:05 UTC&quot;}
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
curl -g "http://localhost:3000/api/v1/past_actions?by_period[starts_at]=2020-10-25+16%3A56%3A05+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A05+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0NmZlZGZkNC1mYWEyLTQ5ZjktOTE2Ni0wYjViNmI2ODc0MjkiLCJzdWIiOiIxMjMwMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NSwiZXhwIjoxNjA1ODA0OTY1fQ.iAl77Yl-6OLd2rzWmQyVqz3lnxRhkp2TVZj7dMZjQK8"
```
# Agenda Items



## Create agenda item


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/5535/agenda_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwMWY3YmViYi1kODQyLTRjZGEtOGFkZC1lZTMzYWQ5NTgyOTkiLCJzdWIiOiIxMjM2MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NSwiZXhwIjoxNjA1ODA0OTc1fQ.rbD0a6ntaIR-xwzSC9nLPJR53vn_jElBN2aMnmGPFqw
```

`POST /api/v1/meetings/:meeting_id/agenda_items`

#### Parameters


```json
{"data":{"type":"agenda_item","attributes":{"description":"Discuss reticulating the splines.","owner_id":12362,"position":3,"duration_in_mins":15,"started_at":"2020-10-25T16:54:15.011Z"}}}
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
    "id": "2618",
    "type": "agenda_items",
    "attributes": {
      "id": 2618,
      "owner_name": "Cyborg Multiple Vibe",
      "owner_id": 12362,
      "description": "Discuss reticulating the splines.",
      "duration_in_mins": 15,
      "time_spent_in_secs": null,
      "started_at": "2020-10-25T16:54:15.011Z",
      "ended_at": null,
      "meeting_id": 5535,
      "position": 3
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/5535/agenda_items" -d '{"data":{"type":"agenda_item","attributes":{"description":"Discuss reticulating the splines.","owner_id":12362,"position":3,"duration_in_mins":15,"started_at":"2020-10-25T16:54:15.011Z"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwMWY3YmViYi1kODQyLTRjZGEtOGFkZC1lZTMzYWQ5NTgyOTkiLCJzdWIiOiIxMjM2MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NSwiZXhwIjoxNjA1ODA0OTc1fQ.rbD0a6ntaIR-xwzSC9nLPJR53vn_jElBN2aMnmGPFqw"
```
## Delete agenda item


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/5534/agenda_items/2617
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkNDQ4YjU2MC02NjhhLTRlMDktYmU0OS0zNjMzMDcwYjJhNjUiLCJzdWIiOiIxMjM2MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NCwiZXhwIjoxNjA1ODA0OTc0fQ.0d58LJlLhonSKHHoSCYoZQWJyRJPoiECRXP5zFV4TIE
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
curl "http://localhost:3000/api/v1/meetings/5534/agenda_items/2617" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkNDQ4YjU2MC02NjhhLTRlMDktYmU0OS0zNjMzMDcwYjJhNjUiLCJzdWIiOiIxMjM2MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NCwiZXhwIjoxNjA1ODA0OTc0fQ.0d58LJlLhonSKHHoSCYoZQWJyRJPoiECRXP5zFV4TIE"
```
## List agenda items


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/5536/agenda_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmODg3YTZlMC1kYmE0LTRkMDEtYjlmOC05ZjRiMWRlMjQ5ODAiLCJzdWIiOiIxMjM2MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NSwiZXhwIjoxNjA1ODA0OTc1fQ.smAr0Z6B5DvpE7O1Ung627X0k7zl31ngo4qtmpPBNRo
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
curl -g "http://localhost:3000/api/v1/meetings/5536/agenda_items" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmODg3YTZlMC1kYmE0LTRkMDEtYjlmOC05ZjRiMWRlMjQ5ODAiLCJzdWIiOiIxMjM2MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NSwiZXhwIjoxNjA1ODA0OTc1fQ.smAr0Z6B5DvpE7O1Ung627X0k7zl31ngo4qtmpPBNRo"
```
## Show agenda item


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/5537/agenda_items/2619
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3NWM2ZGJkZi0xNWU5LTQwMDMtYTM0OS1hNzI5NzliNTE3ZjAiLCJzdWIiOiIxMjM2NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NSwiZXhwIjoxNjA1ODA0OTc1fQ.ilD_D-AcNHcJkFGAYJ4wYfWdjLm1UqZcC3XyKZs0UhA
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
    "id": "2619",
    "type": "agenda_items",
    "attributes": {
      "id": 2619,
      "owner_name": "Red Groot Mr Jigsaw",
      "owner_id": 12365,
      "description": "Vice bicycle rights cronut.",
      "duration_in_mins": 70,
      "time_spent_in_secs": null,
      "started_at": null,
      "ended_at": null,
      "meeting_id": 5537,
      "position": 1
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/5537/agenda_items/2619" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3NWM2ZGJkZi0xNWU5LTQwMDMtYTM0OS1hNzI5NzliNTE3ZjAiLCJzdWIiOiIxMjM2NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NSwiZXhwIjoxNjA1ODA0OTc1fQ.ilD_D-AcNHcJkFGAYJ4wYfWdjLm1UqZcC3XyKZs0UhA"
```
## Update agenda item


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/5538/agenda_items/2620
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjYWY3MjllZi02ZGFkLTRlYjctYjdhMy01YzA1OWYwMTc3NTEiLCJzdWIiOiIxMjM2NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NSwiZXhwIjoxNjA1ODA0OTc1fQ.72AQwdEtXDe_r6cRWvoKGW3OZeofKTGLMK1laDPriwk
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
    "id": "2620",
    "type": "agenda_items",
    "attributes": {
      "id": 2620,
      "owner_name": "Mystique General Abomination Brain",
      "owner_id": 12367,
      "description": "Talk about things",
      "duration_in_mins": 16,
      "time_spent_in_secs": null,
      "started_at": null,
      "ended_at": null,
      "meeting_id": 5538,
      "position": 1
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/5538/agenda_items/2620" -d '{"data":{"type":"agenda_item","attributes":{"description":"Talk about things"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjYWY3MjllZi02ZGFkLTRlYjctYjdhMy01YzA1OWYwMTc3NTEiLCJzdWIiOiIxMjM2NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NSwiZXhwIjoxNjA1ODA0OTc1fQ.72AQwdEtXDe_r6cRWvoKGW3OZeofKTGLMK1laDPriwk"
```
# Articles



## Create article


### Request

#### Endpoint

```plaintext
POST /api/v1/articles
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0YzZmZTE2MS05ZWE5LTRiMDItYTZhMy0yMjZhZGI3NjM2ZTYiLCJzdWIiOiIxMjMzNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.xacfgg0LjKAGJokr6mMQpjCCmVOmfPli5cBp4vZ5j9E
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
    "id": "267",
    "type": "articles",
    "attributes": {
      "id": 267,
      "title": "Testing",
      "url": "http://www.meetwell.app",
      "pull_quote": null,
      "description": null,
      "position": 5,
      "publish_on": "2020-10-25T16:56:10.195Z",
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0YzZmZTE2MS05ZWE5LTRiMDItYTZhMy0yMjZhZGI3NjM2ZTYiLCJzdWIiOiIxMjMzNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.xacfgg0LjKAGJokr6mMQpjCCmVOmfPli5cBp4vZ5j9E"
```
## Delete article


### Request

#### Endpoint

```plaintext
DELETE /api/v1/articles/268
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmZDUzODkxYy01YmRmLTQ1MjEtYmRmMC1jYzVlOWY0ZjY2ZjAiLCJzdWIiOiIxMjMzNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.yS797Y4olKy2-LMku6ChTRHbfC0gyRBU_7--KiI_0pc
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
curl "http://localhost:3000/api/v1/articles/268" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmZDUzODkxYy01YmRmLTQ1MjEtYmRmMC1jYzVlOWY0ZjY2ZjAiLCJzdWIiOiIxMjMzNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.yS797Y4olKy2-LMku6ChTRHbfC0gyRBU_7--KiI_0pc"
```
## List articles


### Request

#### Endpoint

```plaintext
GET /api/v1/articles
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhNTBhMzUzNS0wNmY0LTQ5MjEtYmE4MC0xODdhZDAwMDk0ZDUiLCJzdWIiOiIxMjMzOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.Ed7iUDAtKCGPZvhxnL6FlSLcUkcd0RzNS_Dguo453YA
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
        "position": 1,
        "publish_on": "2020-10-24T00:24:29.144Z",
        "tag_list": [
          "paul-graham",
          "makers-schedule",
          "defend",
          "focus-block"
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
        "position": 2,
        "publish_on": "2020-10-24T00:24:29.178Z",
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
        "position": 3,
        "publish_on": "2020-10-24T00:24:29.190Z",
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
        "position": 4,
        "publish_on": "2020-10-24T00:24:29.201Z",
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhNTBhMzUzNS0wNmY0LTQ5MjEtYmE4MC0xODdhZDAwMDk0ZDUiLCJzdWIiOiIxMjMzOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.Ed7iUDAtKCGPZvhxnL6FlSLcUkcd0RzNS_Dguo453YA"
```
## Show article


### Request

#### Endpoint

```plaintext
GET /api/v1/articles/270
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5MzZhODI1Yy1lZTgzLTRhOTMtYWZlOS0wM2ZlNzgxM2U5NWIiLCJzdWIiOiIxMjMzNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.o7hYKy1zqXGbtOOmoI4o5KNAecnpCEJMex8ll8E5NdY
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
    "id": "270",
    "type": "articles",
    "attributes": {
      "id": 270,
      "title": "Fixie yuccie loko seitan vhs banjo ennui brooklyn.",
      "url": "http://mayert-daniel.org/dylan.gerlach",
      "pull_quote": "Williamsburg authentic goth 3 wolf moon listicle mustache next level locavore bespoke butcher xoxo.",
      "description": null,
      "position": 5,
      "publish_on": "2020-10-25T16:56:10.592Z",
      "tag_list": [
        "tool-tip",
        "test"
      ]
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/articles/270" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5MzZhODI1Yy1lZTgzLTRhOTMtYWZlOS0wM2ZlNzgxM2U5NWIiLCJzdWIiOiIxMjMzNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.o7hYKy1zqXGbtOOmoI4o5KNAecnpCEJMex8ll8E5NdY"
```
## Update article


### Request

#### Endpoint

```plaintext
PUT /api/v1/articles/269
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmODJmMjg2ZS1kNjM4LTRjZDAtODgyMC01NGIxYWJjMWQ1NmQiLCJzdWIiOiIxMjMzNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.NgXAfOJ86SGtfTv-nwbLfpq_Udg2uHNCBYuYch4OYEc
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
    "id": "269",
    "type": "articles",
    "attributes": {
      "id": 269,
      "title": "Testing again",
      "url": "http://hilll.info/rudolph",
      "pull_quote": "Cred hella jean shorts readymade lo-fi sartorial knausgaard tofu health trust fund chartreuse diy meditation.",
      "description": null,
      "position": 5,
      "publish_on": "2020-10-25T16:56:10.461Z",
      "tag_list": [
        "tool-tip",
        "test"
      ]
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/articles/269" -d '{"data":{"type":"article","attributes":{"title":"Testing again"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmODJmMjg2ZS1kNjM4LTRjZDAtODgyMC01NGIxYWJjMWQ1NmQiLCJzdWIiOiIxMjMzNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.NgXAfOJ86SGtfTv-nwbLfpq_Udg2uHNCBYuYch4OYEc"
```
# Attendees



## Create attendee


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/5540/attendees
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MjM1ODFkMi1iYmU2LTRjMGYtYWVmNS0zOTc2MzJiMjI4MzkiLCJzdWIiOiIxMjM3NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NywiZXhwIjoxNjA1ODA0OTc3fQ.MULKihyEUC23Uvg9WkWn-HDIBUjUgZm39-byI8ehCdE
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
    "id": "5663",
    "type": "attendees",
    "attributes": {
      "id": 5663,
      "email": "test@test.com",
      "status": "confirmed",
      "role": null,
      "attendee_name": null
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/5540/attendees" -d '{"data":{"type":"attendee","attributes":{"email":"test@test.com","attendee_name":"Test","status":"confirmed"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MjM1ODFkMi1iYmU2LTRjMGYtYWVmNS0zOTc2MzJiMjI4MzkiLCJzdWIiOiIxMjM3NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NywiZXhwIjoxNjA1ODA0OTc3fQ.MULKihyEUC23Uvg9WkWn-HDIBUjUgZm39-byI8ehCdE"
```
## Delete agenda item


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/5539/attendees/5662
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmNzZkOGY5NC1iN2IwLTRiYTktYTc0MS03MzM0ZTY3NTc4N2QiLCJzdWIiOiIxMjM3MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NiwiZXhwIjoxNjA1ODA0OTc2fQ.BaXPJR99bOEqMyWitSZdcajfd2Z1xoR9tik0DE1oelM
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
curl "http://localhost:3000/api/v1/meetings/5539/attendees/5662" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJmNzZkOGY5NC1iN2IwLTRiYTktYTc0MS03MzM0ZTY3NTc4N2QiLCJzdWIiOiIxMjM3MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NiwiZXhwIjoxNjA1ODA0OTc2fQ.BaXPJR99bOEqMyWitSZdcajfd2Z1xoR9tik0DE1oelM"
```
## List attendees


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/5542/attendees
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzMTZmNDMzYi0xMjA4LTRiNGUtOWU3MS1iNDEzYmVkMjE3ZDEiLCJzdWIiOiIxMjM3NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NywiZXhwIjoxNjA1ODA0OTc3fQ.cncBwh8xlxoRkAvlib8xeW7QmZQTvdBl3EyM9aFMdzk
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
curl -g "http://localhost:3000/api/v1/meetings/5542/attendees" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzMTZmNDMzYi0xMjA4LTRiNGUtOWU3MS1iNDEzYmVkMjE3ZDEiLCJzdWIiOiIxMjM3NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NywiZXhwIjoxNjA1ODA0OTc3fQ.cncBwh8xlxoRkAvlib8xeW7QmZQTvdBl3EyM9aFMdzk"
```
## Show attendee


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/5541/attendees/5664
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwMGFiZDZkYi04YTZhLTQyYmEtYmIzYi1kZjRjYmI0ODRmZjciLCJzdWIiOiIxMjM3NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NywiZXhwIjoxNjA1ODA0OTc3fQ.2AZ5gpkm2YkLWD6S6nj6uXEOwWZmGbQ5gKqbJ_iaZes
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
    "id": "5664",
    "type": "attendees",
    "attributes": {
      "id": 5664,
      "email": "raelene.marquardt@heathcote-connelly.com",
      "status": "confirmed",
      "role": "subject_matter_expert",
      "attendee_name": null
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/5541/attendees/5664" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwMGFiZDZkYi04YTZhLTQyYmEtYmIzYi1kZjRjYmI0ODRmZjciLCJzdWIiOiIxMjM3NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NywiZXhwIjoxNjA1ODA0OTc3fQ.2AZ5gpkm2YkLWD6S6nj6uXEOwWZmGbQ5gKqbJ_iaZes"
```
## Update attendee


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/5543/attendees/5665
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYjVhMWE0My03ODljLTQ4ZTYtOGVlYy01YTZhODczYWRkNjYiLCJzdWIiOiIxMjM3OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NywiZXhwIjoxNjA1ODA0OTc3fQ.gEIK004sMo70BSNPcp9CtOIxgH9NdOZQdzPS_XbYuE4
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
    "id": "5665",
    "type": "attendees",
    "attributes": {
      "id": 5665,
      "email": "nettie@kulas-conroy.net",
      "status": "confirmed",
      "role": "subject_matter_expert",
      "attendee_name": null
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/5543/attendees/5665" -d '{"data":{"type":"attendee","attributes":{"attendee_name":"Test 2"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYjVhMWE0My03ODljLTQ4ZTYtOGVlYy01YTZhODczYWRkNjYiLCJzdWIiOiIxMjM3OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NywiZXhwIjoxNjA1ODA0OTc3fQ.gEIK004sMo70BSNPcp9CtOIxgH9NdOZQdzPS_XbYuE4"
```
# Calendars



## List added calendars


### Request

#### Endpoint

```plaintext
GET /api/v1/calendars
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYTAyMjkxYS00ZDI2LTRjMTAtYTA4Yi0zN2VlM2YxOTllYWYiLCJzdWIiOiIxMjM4MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OCwiZXhwIjoxNjA1ODA0OTc4fQ.pp6zl_Olqtj3eeUume5llmivZaURKC3CP-TiOwowvOo
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
      "id": "14118",
      "type": "calendars",
      "attributes": {
        "name": "General Wasp",
        "primary": false,
        "source": "google",
        "uuid": "29a9ff62-75f9-4f55-a117-c328bf7c55d2",
        "watching": false
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/calendars" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYTAyMjkxYS00ZDI2LTRjMTAtYTA4Yi0zN2VlM2YxOTllYWYiLCJzdWIiOiIxMjM4MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OCwiZXhwIjoxNjA1ODA0OTc4fQ.pp6zl_Olqtj3eeUume5llmivZaURKC3CP-TiOwowvOo"
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
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiM2ZkZGViNi01N2JmLTQwZmQtODQ3OC0xMGJiYTQ1NDZlYjYiLCJzdWIiOiIxMjMwMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NSwiZXhwIjoxNjA1ODA0OTY1fQ.qedT7fJD_0vnCNjmtDwih13c1HC_qAORV0rbPNXoQ1w
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
        "position": 11
      }
    },
    {
      "id": "1",
      "type": "goals",
      "attributes": {
        "key": "be_creative",
        "name": "🎨 Be creative",
        "position": 1
      }
    },
    {
      "id": "6",
      "type": "goals",
      "attributes": {
        "key": "be_strategic",
        "name": "📆 Be more strategic",
        "position": 6
      }
    },
    {
      "id": "8",
      "type": "goals",
      "attributes": {
        "key": "exercise",
        "name": "💪 Exercise",
        "position": 8
      }
    },
    {
      "id": "5",
      "type": "goals",
      "attributes": {
        "key": "get_things_done",
        "name": "🖋 Get things done",
        "position": 5
      }
    },
    {
      "id": "3",
      "type": "goals",
      "attributes": {
        "key": "hang_with_kids",
        "name": "😎 Hang with the kids",
        "position": 3
      }
    },
    {
      "id": "2",
      "type": "goals",
      "attributes": {
        "key": "learn_something",
        "name": "🏄 Learn something new",
        "position": 2
      }
    },
    {
      "id": "9",
      "type": "goals",
      "attributes": {
        "key": "meditate",
        "name": "😌 Meditate",
        "position": 9
      }
    },
    {
      "id": "10",
      "type": "goals",
      "attributes": {
        "key": "sleep",
        "name": "😪 Sleep",
        "position": 10
      }
    },
    {
      "id": "12",
      "type": "goals",
      "attributes": {
        "key": "sports",
        "name": "⚾️ Watch sports",
        "position": 12
      }
    },
    {
      "id": "7",
      "type": "goals",
      "attributes": {
        "key": "take_time_off",
        "name": "⏱ Take some time off",
        "position": 7
      }
    },
    {
      "id": "4",
      "type": "goals",
      "attributes": {
        "key": "time_with_spouse",
        "name": "😘 Spend time with your partner",
        "position": 4
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/goals" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiM2ZkZGViNi01N2JmLTQwZmQtODQ3OC0xMGJiYTQ1NDZlYjYiLCJzdWIiOiIxMjMwMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NSwiZXhwIjoxNjA1ODA0OTY1fQ.qedT7fJD_0vnCNjmtDwih13c1HC_qAORV0rbPNXoQ1w"
```
# Google Calendar



## List Google Calendars


### Request

#### Endpoint

```plaintext
GET /api/v1/google_calendar/list
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxNjAwYzY4OC01OWI0LTQ0ZTctYmVjNS1mZDgwZjlmMzJmMWMiLCJzdWIiOiIxMjI3MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MSwiZXhwIjoxNjA1ODA0OTYxfQ.wfQXsLZY54RnrxJ233fTM3KGJRm1ZXFxRjLNFDUQH0I
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxNjAwYzY4OC01OWI0LTQ0ZTctYmVjNS1mZDgwZjlmMzJmMWMiLCJzdWIiOiIxMjI3MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MSwiZXhwIjoxNjA1ODA0OTYxfQ.wfQXsLZY54RnrxJ233fTM3KGJRm1ZXFxRjLNFDUQH0I"
```
## Setup Google Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/google_calendar/webhooks_setup
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1YzA5YzJmYS0wM2RlLTQ2ZjQtYTZhNy1hMWQ2NTE3NTBjMmMiLCJzdWIiOiIxMjM2OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NiwiZXhwIjoxNjA1ODA0OTc2fQ.FlAyOIGWzMvF5ghh4z7WyA8aoV9DwwXZMgB82iZKzQU
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1YzA5YzJmYS0wM2RlLTQ2ZjQtYTZhNy1hMWQ2NTE3NTBjMmMiLCJzdWIiOiIxMjM2OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NiwiZXhwIjoxNjA1ODA0OTc2fQ.FlAyOIGWzMvF5ghh4z7WyA8aoV9DwwXZMgB82iZKzQU"
```
## Stop Google Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/google_calendar/webhooks_stop
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4YmVmZjlhNC0wM2I1LTQ1ZTEtYjBkNy05MDNmMDVlNTVjOGYiLCJzdWIiOiIxMjM2OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NiwiZXhwIjoxNjA1ODA0OTc2fQ.jocxASdNTyc2uVpFQUAInQuOLxbPfWmLYim9NiM7Zjs
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4YmVmZjlhNC0wM2I1LTQ1ZTEtYjBkNy05MDNmMDVlNTVjOGYiLCJzdWIiOiIxMjM2OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NiwiZXhwIjoxNjA1ODA0OTc2fQ.jocxASdNTyc2uVpFQUAInQuOLxbPfWmLYim9NiM7Zjs"
```
## Watch Google Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/google_calendar/events/watch
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiODc2MTA4Ny0zOTNjLTQwZmEtYTEzNS1iOWE2Yjc5ODAwNWUiLCJzdWIiOiIxMjM3MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NiwiZXhwIjoxNjA1ODA0OTc2fQ.o_QK56uuAtbd9CHLWqyuW0aGZwAjvKZUNf3wSOLTIsE
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiODc2MTA4Ny0zOTNjLTQwZmEtYTEzNS1iOWE2Yjc5ODAwNWUiLCJzdWIiOiIxMjM3MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NiwiZXhwIjoxNjA1ODA0OTc2fQ.o_QK56uuAtbd9CHLWqyuW0aGZwAjvKZUNf3wSOLTIsE" \
	-H "X-Goog-Channel: f8ed7692-4865-4240-81f4-c0d82677f51b" \
	-H "X-Goog-Resource: c3f3224c-36a3-4888-afd2-6e950a9a957b"
```
# Invoices



## Get invoices


### Request

#### Endpoint

```plaintext
GET /api/v1/invoices
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhNGRkYTc0Zi03NzQ3LTQ2M2UtOTdmOS05ZTNiNTJiMTg2NjgiLCJzdWIiOiIxMjMzOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.cXDT3qrV3I0PUpTTN_EnZzSN7NpDeCmO0dLgEEEaJlc
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhNGRkYTc0Zi03NzQ3LTQ2M2UtOTdmOS05ZTNiNTJiMTg2NjgiLCJzdWIiOiIxMjMzOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.cXDT3qrV3I0PUpTTN_EnZzSN7NpDeCmO0dLgEEEaJlc"
```
# Meeting Categories



## List meeting categories


### Request

#### Endpoint

```plaintext
GET /api/v1/meeting_categories
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0YzIzNDI2Ni1iODg2LTQ1Y2ItOThjZi1jYTYxYWVmNDI4NzMiLCJzdWIiOiIxMjMwMSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NSwiZXhwIjoxNjA1ODA0OTY1fQ.-2A_Du1g9L4l_BBv7B6_-jrGO1vX_snk0C_Q_F998rs
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
    "id": "a2eed570-7979-4d18-968d-ce2091b53453",
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0YzIzNDI2Ni1iODg2LTQ1Y2ItOThjZi1jYTYxYWVmNDI4NzMiLCJzdWIiOiIxMjMwMSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NSwiZXhwIjoxNjA1ODA0OTY1fQ.-2A_Du1g9L4l_BBv7B6_-jrGO1vX_snk0C_Q_F998rs"
```
# Meeting Intentions



## List meeting intentions


### Request

#### Endpoint

```plaintext
GET /api/v1/meeting_intentions
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzN2VkNjAyYy04MWMzLTRkOTktODEyYi00OGJjM2ZlOWUwOTYiLCJzdWIiOiIxMjQwOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.h8i6fdUvDLZoG3tqGWGTHkqBi-C8Y3MwazSD0aOqD3Q
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
    "id": "02ca5dd2-05ab-4def-a880-9eff1032c476",
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzN2VkNjAyYy04MWMzLTRkOTktODEyYi00OGJjM2ZlOWUwOTYiLCJzdWIiOiIxMjQwOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.h8i6fdUvDLZoG3tqGWGTHkqBi-C8Y3MwazSD0aOqD3Q"
```
# Meetings



## Accept a meeting invite


### Request

#### Endpoint

```plaintext
GET /api/v1/users/meetings/accept/5548
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlYWYzMGRlYy1lZmQ5LTRmNTQtOTE1NS0zZjhlZTYxNzM0MWUiLCJzdWIiOiIxMjM5OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MCwiZXhwIjoxNjA1ODA0OTgwfQ.0WFt0RXIWJ6Z7JHITCyHsra5JGpXOtwmrXdnPO7J2Uc
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
    "id": "3796",
    "type": "user_meetings",
    "attributes": {
      "non_compliance_action": null,
      "organizer_notes": null,
      "meeting_id": 5548,
      "user_id": 12399,
      "token": "pWKBHVMbqBuRgNANmCwYNKVF"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/users/meetings/accept/5548" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlYWYzMGRlYy1lZmQ5LTRmNTQtOTE1NS0zZjhlZTYxNzM0MWUiLCJzdWIiOiIxMjM5OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MCwiZXhwIjoxNjA1ODA0OTgwfQ.0WFt0RXIWJ6Z7JHITCyHsra5JGpXOtwmrXdnPO7J2Uc"
```
## Convert meeting to focus block


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/5531/make_focus_block?by_period[starts_at]=2020-10-25+16%3A56%3A13+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A13+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxMzVjZWNlZS02MGU2LTQxM2UtYjhhNS0zOWZiZjY0NzY0MTEiLCJzdWIiOiIxMjM1MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MywiZXhwIjoxNjA1ODA0OTczfQ.sA6uAOg-37QuHSwcZlNxNNIEerS73kRlECkFlFKEuxo
```

`GET /api/v1/meetings/:id/make_focus_block`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:13 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:13 UTC&quot;}
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
    "id": "454",
    "type": "focus_blocks",
    "attributes": {
      "label": "Coding",
      "category": "focus",
      "calendar_id": 14084,
      "recurring_meeting_uuid": "6vkb5i9kqmu36jr1t0v48lkcrk",
      "duration": 3600,
      "starts_at": "2020-10-19T22:03:00.000Z",
      "ends_at": "2020-10-19T23:03:00.000Z",
      "rrule": "RRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA",
      "recurring": true
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/5531/make_focus_block?by_period[starts_at]=2020-10-25+16%3A56%3A13+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A13+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxMzVjZWNlZS02MGU2LTQxM2UtYjhhNS0zOWZiZjY0NzY0MTEiLCJzdWIiOiIxMjM1MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MywiZXhwIjoxNjA1ODA0OTczfQ.sA6uAOg-37QuHSwcZlNxNNIEerS73kRlECkFlFKEuxo"
```
## Convert meeting to life block


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/5533/make_life_block?by_period[starts_at]=2020-10-25+16%3A56%3A14+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A14+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyYjA1M2I5Yy02OWVjLTRlNjEtODM2Yi05NzViZGY0OTk5M2EiLCJzdWIiOiIxMjM1NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NCwiZXhwIjoxNjA1ODA0OTc0fQ.XEUk7FwP3YiHy-DuQ9ukl2XKboYsIMNraygY1RzPPrE
```

`GET /api/v1/meetings/:id/make_life_block`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:14 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:14 UTC&quot;}
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
    "id": "455",
    "type": "focus_blocks",
    "attributes": {
      "label": "Coding",
      "category": "life",
      "calendar_id": 14088,
      "recurring_meeting_uuid": "6vkb5i9kqmu36jr1t0v48lkcrk",
      "duration": 3600,
      "starts_at": "2020-10-19T22:03:00.000Z",
      "ends_at": "2020-10-19T23:03:00.000Z",
      "rrule": "RRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA",
      "recurring": true
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/5533/make_life_block?by_period[starts_at]=2020-10-25+16%3A56%3A14+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A14+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyYjA1M2I5Yy02OWVjLTRlNjEtODM2Yi05NzViZGY0OTk5M2EiLCJzdWIiOiIxMjM1NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NCwiZXhwIjoxNjA1ODA0OTc0fQ.XEUk7FwP3YiHy-DuQ9ukl2XKboYsIMNraygY1RzPPrE"
```
## List meetings


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings?by_period[starts_at]=2020-10-25+16%3A56%3A12+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A12+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhZWJjMTA2Yi02ZDBjLTQwY2EtYTAzMi0yZWZlNDY3YmQwNDgiLCJzdWIiOiIxMjM0NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MiwiZXhwIjoxNjA1ODA0OTcyfQ.nbbZsBPrc32yyjYgoIbrUEHORWQdlvE73oB9DIFqK3I
```

`GET /api/v1/meetings`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:12 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:12 UTC&quot;}
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
      "id": "5529",
      "type": "meetings",
      "attributes": {
        "summary": "Cleanse kombucha locavore dreamcatcher taxidermy umami heirloom keytar.",
        "description": "Voluptatem dolorum commodi. Necessitatibus exercitationem quia. Quisquam ad nesciunt. Consequuntur non et.",
        "starts_at": "2020-10-25T17:01:12.177Z",
        "ends_at": "2020-10-25T18:01:12.177Z",
        "category_list": [

        ],
        "location": "46137 Ayanna Brooks, Port Raphaelton, WY 19283",
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
curl -g "http://localhost:3000/api/v1/meetings?by_period[starts_at]=2020-10-25+16%3A56%3A12+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A12+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhZWJjMTA2Yi02ZDBjLTQwY2EtYTAzMi0yZWZlNDY3YmQwNDgiLCJzdWIiOiIxMjM0NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MiwiZXhwIjoxNjA1ODA0OTcyfQ.nbbZsBPrc32yyjYgoIbrUEHORWQdlvE73oB9DIFqK3I"
```
## Meeting details for unauthenticated organizer


### Request

#### Endpoint

```plaintext
GET /api/v1/users/meetings/details/RsTqbtbaFJSMxXbyoxcLQutj
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjODM4MzFhYi1jM2UwLTQ4NWMtOGNkYi00MDNjN2I3YThmYTIiLCJzdWIiOiIxMjM5MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OSwiZXhwIjoxNjA1ODA0OTc5fQ.er12kv_8UBXEp6CsNd2QGKRzJ2T90JxaZaZEEdykiEo
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
    "id": "5546",
    "type": "meetings",
    "attributes": {
      "summary": "Helvetica brunch tousled wes anderson.",
      "description": "Sit eum autem. Commodi facere ea. Recusandae aliquid est. Illo perspiciatis saepe.",
      "starts_at": "2020-10-25T17:01:19.670Z",
      "ends_at": "2020-10-25T18:01:19.670Z",
      "category_list": [

      ],
      "intention": null,
      "location": "8392 Brekke Estates, Rathhaven, NE 79268-0407",
      "duration": 3600,
      "maybe_focus_block": false,
      "maybe_life_block": false,
      "status": null,
      "edit_permission": true,
      "wellness_block_id": null,
      "event_report_card_id": null,
      "compliance_deadline": "2020-10-25T11:01:19.670Z",
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
          "email": "harlan.littel@bosco.name",
          "domain": "bosco.name",
          "role": "subject_matter_expert"
        },
        {
          "email": "anisa.cormier@stanton.biz",
          "domain": "stanton.biz",
          "role": "subject_matter_expert"
        }
      ],
      "attendees_count": 2,
      "cost": 76.0,
      "recurring_meeting": false,
      "score": 34,
      "results": null,
      "quality_label": "An F? Is that what you feel your time is worth?",
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
curl -g "http://localhost:3000/api/v1/users/meetings/details/RsTqbtbaFJSMxXbyoxcLQutj" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjODM4MzFhYi1jM2UwLTQ4NWMtOGNkYi00MDNjN2I3YThmYTIiLCJzdWIiOiIxMjM5MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OSwiZXhwIjoxNjA1ODA0OTc5fQ.er12kv_8UBXEp6CsNd2QGKRzJ2T90JxaZaZEEdykiEo"
```
## Organizer prevents a decline


### Request

#### Endpoint

```plaintext
PUT /api/v1/users/meetings/prevent_decline/DipnT2yUX5A7RCR94yUzHwRU
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2NDk3MTcyYy03Nzk4LTQ2MzYtOWNiOC1lNThiYzVlNzJmNTgiLCJzdWIiOiIxMjM5NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MCwiZXhwIjoxNjA1ODA0OTgwfQ.hnl6nCjXDMHKxT5ByaVXHGDxznopFDDzp3_y81RvP48
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
    "id": "3795",
    "type": "user_meetings",
    "attributes": {
      "non_compliance_action": "do nothing",
      "organizer_notes": "Testing!",
      "meeting_id": 5547,
      "user_id": 12396,
      "token": "DipnT2yUX5A7RCR94yUzHwRU"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/users/meetings/prevent_decline/DipnT2yUX5A7RCR94yUzHwRU" -d '{"data":{"type":"user_meeting","attributes":{"organizer_notes":"Testing!"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2NDk3MTcyYy03Nzk4LTQ2MzYtOWNiOC1lNThiYzVlNzJmNTgiLCJzdWIiOiIxMjM5NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MCwiZXhwIjoxNjA1ODA0OTgwfQ.hnl6nCjXDMHKxT5ByaVXHGDxznopFDDzp3_y81RvP48"
```
## Show meeting evaluation


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/5530/evaluate?by_period[starts_at]=2020-10-25+16%3A56%3A12+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A12+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlOTAzMWFhZi0yZTQzLTQ2NGYtYTNmMi0wZjgwMWI3NmY3MjMiLCJzdWIiOiIxMjM0OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MiwiZXhwIjoxNjA1ODA0OTcyfQ.89faTvhmud9dnPaUtgtU6AMGcfH5g1tB13gdGcRyX2A
```

`GET /api/v1/meetings/:id/evaluate`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:12 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:12 UTC&quot;}
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
    "id": "5530",
    "type": "meetings",
    "attributes": {
      "summary": "Brunch hella occupy celiac.",
      "description": "Impedit voluptates consequuntur. Aut qui sapiente. Voluptatem eos perferendis. Nisi ut officia.",
      "starts_at": "2020-10-25T17:01:12.521Z",
      "ends_at": "2020-10-25T18:01:12.521Z",
      "category_list": [

      ],
      "intention": null,
      "location": "Suite 369 297 George Field, Monikachester, MA 50141-6704",
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
          "email": "napoleon_mohr@borer.co",
          "domain": "borer.co",
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
curl -g "http://localhost:3000/api/v1/meetings/5530/evaluate?by_period[starts_at]=2020-10-25+16%3A56%3A12+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A12+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlOTAzMWFhZi0yZTQzLTQ2NGYtYTNmMi0wZjgwMWI3NmY3MjMiLCJzdWIiOiIxMjM0OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MiwiZXhwIjoxNjA1ODA0OTcyfQ.89faTvhmud9dnPaUtgtU6AMGcfH5g1tB13gdGcRyX2A"
```
## Show user meeting


### Request

#### Endpoint

```plaintext
GET /api/v1/users/meetings/5544
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyZThiN2U1My01NDVkLTQ2OTItODE5Zi1jNzM0MWQ2OGExODAiLCJzdWIiOiIxMjM4NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OSwiZXhwIjoxNjA1ODA0OTc5fQ.HDFWD6DcGXlc0xMu1reqXJZrAQ95PleXYI0YRfIUShw
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
    "id": "3792",
    "type": "user_meetings",
    "attributes": {
      "non_compliance_action": null,
      "organizer_notes": null,
      "meeting_id": 5544,
      "user_id": 12387,
      "token": "uvjc6DtcgnzSfXE6twKjoKmE"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/users/meetings/5544" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyZThiN2U1My01NDVkLTQ2OTItODE5Zi1jNzM0MWQ2OGExODAiLCJzdWIiOiIxMjM4NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OSwiZXhwIjoxNjA1ODA0OTc5fQ.HDFWD6DcGXlc0xMu1reqXJZrAQ95PleXYI0YRfIUShw"
```
## Update meeting


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/5532
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3MjBmZmE0ZS1lZTNkLTQ0ZmMtYWJhYi1jN2ExODE1NDhiYTUiLCJzdWIiOiIxMjM1MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MywiZXhwIjoxNjA1ODA0OTczfQ.kUju2KGY3uwmwGnbu5oawSl-NKH6UufEBioBrS1ya9w
```

`PUT /api/v1/meetings/:id`

#### Parameters


```json
{"by_period":{"starts_at":"2020-10-25T16:56:13.807Z","ends_at":"2020-11-01T16:56:13.807Z"},"data":{"type":"agenda_item","attributes":{"started_at":"2020-10-25T16:36:13.807Z","ended_at":"2020-10-25T16:56:13.807Z"}}}
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
    "id": "5532",
    "type": "meetings",
    "attributes": {
      "summary": "Kogi cleanse raw denim.",
      "description": "Velit delectus fugit. Nihil repellendus aut. Cum eum qui. Eius in quidem.",
      "starts_at": "2020-10-25T17:01:13.654Z",
      "ends_at": "2020-10-25T18:01:13.654Z",
      "category_list": [

      ],
      "intention": null,
      "location": "Suite 268 115 Heike Summit, Sherrylhaven, NJ 57169",
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
          "email": "claudie.rowe@weber-gusikowski.biz",
          "domain": "weber-gusikowski.biz",
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
curl "http://localhost:3000/api/v1/meetings/5532" -d '{"by_period":{"starts_at":"2020-10-25T16:56:13.807Z","ends_at":"2020-11-01T16:56:13.807Z"},"data":{"type":"agenda_item","attributes":{"started_at":"2020-10-25T16:36:13.807Z","ended_at":"2020-10-25T16:56:13.807Z"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3MjBmZmE0ZS1lZTNkLTQ0ZmMtYWJhYi1jN2ExODE1NDhiYTUiLCJzdWIiOiIxMjM1MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MywiZXhwIjoxNjA1ODA0OTczfQ.kUju2KGY3uwmwGnbu5oawSl-NKH6UufEBioBrS1ya9w"
```
## Update user meeting


### Request

#### Endpoint

```plaintext
PUT /api/v1/users/meetings/5545
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5ODZkZjEzYi1iNDVmLTRjOWYtYjZkNy1mMTA3NzdhOWI2YWMiLCJzdWIiOiIxMjM5MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OSwiZXhwIjoxNjA1ODA0OTc5fQ.RIBieqyeYfa_VE5zF-VbqwPtiHr6IQ79BfX3zPesmcs
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
    "id": "3793",
    "type": "user_meetings",
    "attributes": {
      "non_compliance_action": "decline",
      "organizer_notes": null,
      "meeting_id": 5545,
      "user_id": 12390,
      "token": "9nH1S5GUtkLUYffoLrHYEmHF"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/users/meetings/5545" -d '{"data":{"type":"user_meeting","attributes":{"non_compliance_action":"decline"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5ODZkZjEzYi1iNDVmLTRjOWYtYjZkNy1mMTA3NzdhOWI2YWMiLCJzdWIiOiIxMjM5MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OSwiZXhwIjoxNjA1ODA0OTc5fQ.RIBieqyeYfa_VE5zF-VbqwPtiHr6IQ79BfX3zPesmcs"
```
# Microsoft Outlook



## List Outlook Calendars


### Request

#### Endpoint

```plaintext
GET /api/v1/microsoft_outlook/list
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NjMzOWE4Mi0xODJmLTRmMTktODEyNS0wZGVhMzgwNjkzNjYiLCJzdWIiOiIxMjQwOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.mqfiVkBOpTboxlLfUk1EtzXDE5TNOFxEl-75BTNqgHc
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NjMzOWE4Mi0xODJmLTRmMTktODEyNS0wZGVhMzgwNjkzNjYiLCJzdWIiOiIxMjQwOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.mqfiVkBOpTboxlLfUk1EtzXDE5TNOFxEl-75BTNqgHc"
```
## Setup Outlook Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/microsoft_outlook/webhooks_setup
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMGJhOGZkZi0yOGNhLTQ1OWEtODhmMy1lZjA1MTNmZTljNDciLCJzdWIiOiIxMjMzMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OSwiZXhwIjoxNjA1ODA0OTY5fQ._xT-nqkUykVUcusuZXOGNaCEHLsrHRLectD8hC55ncY
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMGJhOGZkZi0yOGNhLTQ1OWEtODhmMy1lZjA1MTNmZTljNDciLCJzdWIiOiIxMjMzMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OSwiZXhwIjoxNjA1ODA0OTY5fQ._xT-nqkUykVUcusuZXOGNaCEHLsrHRLectD8hC55ncY"
```
## Stop Outlook Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/microsoft_outlook/webhooks_stop
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2N2RmZmEzMC01Y2U4LTQ1ZDMtYTYyZi1hMzc2YjliZGNjY2UiLCJzdWIiOiIxMjMzMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.ibzIRJuqP2rQK-gDzB1l7EDafa_Nvdtwf4OuPZqZvrM
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2N2RmZmEzMC01Y2U4LTQ1ZDMtYTYyZi1hMzc2YjliZGNjY2UiLCJzdWIiOiIxMjMzMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.ibzIRJuqP2rQK-gDzB1l7EDafa_Nvdtwf4OuPZqZvrM"
```
## Watch Outlook Webhook


### Request

#### Endpoint

```plaintext
POST /api/v1/microsoft_outlook/events/watch
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlODFkMWNlOC1mODIyLTQ2YTktOWViYS0zYThjNTMwZDYyZTQiLCJzdWIiOiIxMjMzMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OSwiZXhwIjoxNjA1ODA0OTY5fQ.ZEN7Qg-jzsk15oH_DxeiDrM7Xl78xbGOEYswfJ4exzA
```

`POST /api/v1/microsoft_outlook/events/watch`

#### Parameters


```json
{"value":[{"clientState":"0886e225-c62a-42cc-93d3-8de8c4dda89f","subscriptionId":"738a45fd-7980-403d-b574-4b08a9942325"}]}
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
curl "http://localhost:3000/api/v1/microsoft_outlook/events/watch" -d '{"value":[{"clientState":"0886e225-c62a-42cc-93d3-8de8c4dda89f","subscriptionId":"738a45fd-7980-403d-b574-4b08a9942325"}]}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlODFkMWNlOC1mODIyLTQ2YTktOWViYS0zYThjNTMwZDYyZTQiLCJzdWIiOiIxMjMzMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OSwiZXhwIjoxNjA1ODA0OTY5fQ.ZEN7Qg-jzsk15oH_DxeiDrM7Xl78xbGOEYswfJ4exzA"
```
## Watch Outlook Webhook Lifecycle


### Request

#### Endpoint

```plaintext
POST /api/v1/microsoft_outlook/events/lifecycle
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5YjkyNTY5NC00MGIyLTRkM2YtYjA5OC0zMmYzMWM2OTE4Y2QiLCJzdWIiOiIxMjMyOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OSwiZXhwIjoxNjA1ODA0OTY5fQ.hiP7mLa7GYrJbL68hsCImtgTqGKJEPyb_vtJdmfsuhk
```

`POST /api/v1/microsoft_outlook/events/lifecycle`

#### Parameters


```json
{"value":[{"clientState":"bca67577-0e09-4390-9eef-509d4767ca40","subscriptionId":"650f4840-1487-4e14-b9b5-64415974e65a"}]}
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
curl "http://localhost:3000/api/v1/microsoft_outlook/events/lifecycle" -d '{"value":[{"clientState":"bca67577-0e09-4390-9eef-509d4767ca40","subscriptionId":"650f4840-1487-4e14-b9b5-64415974e65a"}]}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI5YjkyNTY5NC00MGIyLTRkM2YtYjA5OC0zMmYzMWM2OTE4Y2QiLCJzdWIiOiIxMjMyOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OSwiZXhwIjoxNjA1ODA0OTY5fQ.hiP7mLa7GYrJbL68hsCImtgTqGKJEPyb_vtJdmfsuhk"
```
# Objectives



## Create objective


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/5523/objectives
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MGE4MGEyMi1kMzQ4LTQ1ODgtOTI3YS04YmYxMWM2YTZjZTgiLCJzdWIiOiIxMjMxNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NywiZXhwIjoxNjA1ODA0OTY3fQ.NlHwAv_oiSX4Z-6a0bO01KMf8lC9wqMIK3BYPmS8R00
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
    "id": "320",
    "type": "objectives",
    "attributes": {
      "meeting_id": 5523,
      "description": "Figure something out",
      "position": 3
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/5523/objectives" -d '{"data":{"type":"objective","attributes":{"description":"Figure something out","position":3}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MGE4MGEyMi1kMzQ4LTQ1ODgtOTI3YS04YmYxMWM2YTZjZTgiLCJzdWIiOiIxMjMxNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NywiZXhwIjoxNjA1ODA0OTY3fQ.NlHwAv_oiSX4Z-6a0bO01KMf8lC9wqMIK3BYPmS8R00"
```
## Delete objective


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/5519/objectives/315
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1YzAwY2RmMy00YmY2LTQyZjAtYWZlYy1kYjA0YjQyOWZkYjMiLCJzdWIiOiIxMjMxMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NywiZXhwIjoxNjA1ODA0OTY3fQ.LxS1lbgNomw5GOUdhoET6z56WsOB14UrGttCkDeszpc
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
curl "http://localhost:3000/api/v1/meetings/5519/objectives/315" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1YzAwY2RmMy00YmY2LTQyZjAtYWZlYy1kYjA0YjQyOWZkYjMiLCJzdWIiOiIxMjMxMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NywiZXhwIjoxNjA1ODA0OTY3fQ.LxS1lbgNomw5GOUdhoET6z56WsOB14UrGttCkDeszpc"
```
## List objectives


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/5522/objectives
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0OWI1OTIxZC00YzkzLTQyODMtYTZlYy00NWI1YzhhNTNlNTYiLCJzdWIiOiIxMjMxNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NywiZXhwIjoxNjA1ODA0OTY3fQ.5cfWLHK4v83a3HUzMNJ4mTSAgEPQyTPP4IupxrRzNHQ
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
      "id": "318",
      "type": "objectives",
      "attributes": {
        "meeting_id": 5522,
        "description": "Deep v try-hard 3 wolf moon wayfarers cornhole plaid marfa distillery cold-pressed aesthetic drinking.",
        "position": 1
      }
    }
  ]
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/5522/objectives" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0OWI1OTIxZC00YzkzLTQyODMtYTZlYy00NWI1YzhhNTNlNTYiLCJzdWIiOiIxMjMxNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NywiZXhwIjoxNjA1ODA0OTY3fQ.5cfWLHK4v83a3HUzMNJ4mTSAgEPQyTPP4IupxrRzNHQ"
```
## Show objective


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/5521/objectives/317
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3NzljYTU1YS03ZmU0LTRiOTAtOTQ0Ny04M2VhZWViNTM1OTciLCJzdWIiOiIxMjMxNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NywiZXhwIjoxNjA1ODA0OTY3fQ.YKLVG79yN4bTA-xOetj7-cwa_rMvNY1UVLjT0Bz6ZpI
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
    "id": "317",
    "type": "objectives",
    "attributes": {
      "meeting_id": 5521,
      "description": "Stumptown tousled vegan meh asymmetrical hammock tacos.",
      "position": 1
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/5521/objectives/317" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3NzljYTU1YS03ZmU0LTRiOTAtOTQ0Ny04M2VhZWViNTM1OTciLCJzdWIiOiIxMjMxNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NywiZXhwIjoxNjA1ODA0OTY3fQ.YKLVG79yN4bTA-xOetj7-cwa_rMvNY1UVLjT0Bz6ZpI"
```
## Update objective


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/5520/objectives/316
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3ZjI5Njc2ZS02NjFkLTQxN2MtOThjYi0zMDI4NzcyYzY4ODgiLCJzdWIiOiIxMjMxMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NywiZXhwIjoxNjA1ODA0OTY3fQ.ztT0gUnafKjzeoNRkds9Esj9uby7TLTZFTaALeBtSzo
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
    "id": "316",
    "type": "objectives",
    "attributes": {
      "meeting_id": 5520,
      "description": "Figure it all out",
      "position": 1
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/5520/objectives/316" -d '{"data":{"type":"objective","attributes":{"description":"Figure it all out"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3ZjI5Njc2ZS02NjFkLTQxN2MtOThjYi0zMDI4NzcyYzY4ODgiLCJzdWIiOiIxMjMxMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NywiZXhwIjoxNjA1ODA0OTY3fQ.ztT0gUnafKjzeoNRkds9Esj9uby7TLTZFTaALeBtSzo"
```
# Organizer Deny-List



## Bulk create deny-list entries


### Request

#### Endpoint

```plaintext
POST /api/v1/users/blacklist_organizers/bulk
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0ZTEwMjRmNi0zZGUyLTRkNjktODgxZC01Njc1MGY5MTZlNmEiLCJzdWIiOiIxMjMxOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.P8JvmEPYwYBF8xU8ZGd17TDoKgNGBUwcAkJiOmF_n_U
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
      "id": "206",
      "type": "blacklist_organizers",
      "attributes": {
        "email": "test@test.com"
      }
    },
    {
      "id": "207",
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0ZTEwMjRmNi0zZGUyLTRkNjktODgxZC01Njc1MGY5MTZlNmEiLCJzdWIiOiIxMjMxOSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.P8JvmEPYwYBF8xU8ZGd17TDoKgNGBUwcAkJiOmF_n_U"
```
## Create deny-list entry


### Request

#### Endpoint

```plaintext
POST /api/v1/users/blacklist_organizers
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlYzlmZTUzZi0xZGY2LTQ2ZTQtODE3Zi04MWRjNjZkMjBmMDUiLCJzdWIiOiIxMjMyMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.pUkXFN3qvrgLQw21PpGQpSRSvI_i23VxNHd4A7k6wkM
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
    "id": "208",
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlYzlmZTUzZi0xZGY2LTQ2ZTQtODE3Zi04MWRjNjZkMjBmMDUiLCJzdWIiOiIxMjMyMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.pUkXFN3qvrgLQw21PpGQpSRSvI_i23VxNHd4A7k6wkM"
```
## List denied organizers


### Request

#### Endpoint

```plaintext
GET /api/v1/users/blacklist_organizers
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3MjhhMTJjNi01NzVjLTQ3OTEtYmVhZS0xYjI1Zjg2NzdmMjEiLCJzdWIiOiIxMjMxNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NywiZXhwIjoxNjA1ODA0OTY3fQ.iz39V_JtHFFgD1_iyiBG5zsawwNbfpJpeS3lKsWjK-s
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3MjhhMTJjNi01NzVjLTQ3OTEtYmVhZS0xYjI1Zjg2NzdmMjEiLCJzdWIiOiIxMjMxNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NywiZXhwIjoxNjA1ODA0OTY3fQ.iz39V_JtHFFgD1_iyiBG5zsawwNbfpJpeS3lKsWjK-s"
```
## Remove denied organizer


### Request

#### Endpoint

```plaintext
DELETE /api/v1/users/blacklist_organizers/205
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3NjVjMDJlZi0wYjhhLTQ2MzAtOTczZS01N2RlYTIwNTJhN2QiLCJzdWIiOiIxMjMxOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.oi6Xai4rA5lgBgouquguAFFwOQiR61m4fhdixd9c3X4
```

`DELETE /api/v1/users/blacklist_organizers/:id`

#### Parameters


None known.


### Response

```plaintext

204 No Content
```




```shell
curl "http://localhost:3000/api/v1/users/blacklist_organizers/205" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3NjVjMDJlZi0wYjhhLTQ2MzAtOTczZS01N2RlYTIwNTJhN2QiLCJzdWIiOiIxMjMxOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.oi6Xai4rA5lgBgouquguAFFwOQiR61m4fhdixd9c3X4"
```
# Ping



## Authenticated Ping


### Request

#### Endpoint

```plaintext
GET /api/v1/ping
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1MGU2Y2Y4Mi1iMjU3LTQzYTktYjM3Yy0yNTQ5MTZjZjNkOGMiLCJzdWIiOiIxMjM0MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.rJTDHxuKxL6SDuJPKzUXMyf-WjLB_PTZ185aAqaOSPU
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
    "id": "5e9be841-bb45-4516-a73e-f49f5375b5bf",
    "type": "pings",
    "attributes": {
      "id": "5e9be841-bb45-4516-a73e-f49f5375b5bf",
      "date": "2020-10-25T16:56:10.989Z"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/ping" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1MGU2Y2Y4Mi1iMjU3LTQzYTktYjM3Yy0yNTQ5MTZjZjNkOGMiLCJzdWIiOiIxMjM0MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MCwiZXhwIjoxNjA1ODA0OTcwfQ.rJTDHxuKxL6SDuJPKzUXMyf-WjLB_PTZ185aAqaOSPU"
```
# Pre-Work Items



## Create prework item


### Request

#### Endpoint

```plaintext
POST /api/v1/meetings/5527/prework_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MjkyNGM2Mi0zYWEwLTRmMDYtYTdlOS04YjczYTI3YTVlOTgiLCJzdWIiOiIxMjM0NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MSwiZXhwIjoxNjA1ODA0OTcxfQ.6OO4qbXVwRm46KXTBYptA_FP0XGZmoaye9GzTtkDUDw
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
    "id": "215",
    "type": "prework_items",
    "attributes": {
      "id": 215,
      "description": "Review the sales report",
      "url": "https://www.locationtofile.com/salesreport.xls",
      "timebox": 3600
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/5527/prework_items" -d '{"data":{"type":"prework_item","attributes":{"description":"Review the sales report","url":"https://www.locationtofile.com/salesreport.xls","timebox":3600}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4MjkyNGM2Mi0zYWEwLTRmMDYtYTdlOS04YjczYTI3YTVlOTgiLCJzdWIiOiIxMjM0NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MSwiZXhwIjoxNjA1ODA0OTcxfQ.6OO4qbXVwRm46KXTBYptA_FP0XGZmoaye9GzTtkDUDw"
```
## Delete prework item


### Request

#### Endpoint

```plaintext
DELETE /api/v1/meetings/5528/prework_items/216
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlOWNlYWMyNS1hNDMzLTQ4M2ItYTc0Yy02YmFlMmRlYmE3NzUiLCJzdWIiOiIxMjM0NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MiwiZXhwIjoxNjA1ODA0OTcyfQ.hIeERTv4NDQ_F5vnVwZpMJ5lpS4bLG_f5bEs1xmITOg
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
curl "http://localhost:3000/api/v1/meetings/5528/prework_items/216" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlOWNlYWMyNS1hNDMzLTQ4M2ItYTc0Yy02YmFlMmRlYmE3NzUiLCJzdWIiOiIxMjM0NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MiwiZXhwIjoxNjA1ODA0OTcyfQ.hIeERTv4NDQ_F5vnVwZpMJ5lpS4bLG_f5bEs1xmITOg"
```
## List prework items


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/5526/prework_items
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4Y2FhOTQ4NS1lZjU0LTRhODMtYTExNi04ZTI3MjdkZjMzNjIiLCJzdWIiOiIxMjM0NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MSwiZXhwIjoxNjA1ODA0OTcxfQ.Nj-y1HP1DHzR-n9DYQUmdt3mcGCakdtD9lyhNJJq2VM
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
curl -g "http://localhost:3000/api/v1/meetings/5526/prework_items" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4Y2FhOTQ4NS1lZjU0LTRhODMtYTExNi04ZTI3MjdkZjMzNjIiLCJzdWIiOiIxMjM0NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MSwiZXhwIjoxNjA1ODA0OTcxfQ.Nj-y1HP1DHzR-n9DYQUmdt3mcGCakdtD9lyhNJJq2VM"
```
## Show prework item


### Request

#### Endpoint

```plaintext
GET /api/v1/meetings/5524/prework_items/213
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3ZjE2OTA1OC0zNDhhLTQ1NWQtOTU2Yy0wOTEyMTNjNGJmOWEiLCJzdWIiOiIxMjM0MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MSwiZXhwIjoxNjA1ODA0OTcxfQ.3ok46qKs5QwiXgorjqxA9pq9CP3mssx5EU-_Ep-xQOg
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
    "id": "213",
    "type": "prework_items",
    "attributes": {
      "id": 213,
      "description": "Tumblr chia readymade mustache.",
      "url": "http://beier.org/cameron.kris",
      "timebox": 3600
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/meetings/5524/prework_items/213" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3ZjE2OTA1OC0zNDhhLTQ1NWQtOTU2Yy0wOTEyMTNjNGJmOWEiLCJzdWIiOiIxMjM0MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MSwiZXhwIjoxNjA1ODA0OTcxfQ.3ok46qKs5QwiXgorjqxA9pq9CP3mssx5EU-_Ep-xQOg"
```
## Update prework item


### Request

#### Endpoint

```plaintext
PUT /api/v1/meetings/5525/prework_items/214
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkYWMxMjNhNy0xMzk1LTQxMmItYjExMy0yZmY4ZmNiZjRkYzkiLCJzdWIiOiIxMjM0MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MSwiZXhwIjoxNjA1ODA0OTcxfQ.8gfZVF17kBzHST-w4QkQugeJqA79BaJjkPJHJX2jopU
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
    "id": "214",
    "type": "prework_items",
    "attributes": {
      "id": 214,
      "description": "Review the sales report dude",
      "url": "http://schowalter-ferry.org/renay",
      "timebox": 3600
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/meetings/5525/prework_items/214" -d '{"data":{"type":"prework_item","attributes":{"description":"Review the sales report dude"}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkYWMxMjNhNy0xMzk1LTQxMmItYjExMy0yZmY4ZmNiZjRkYzkiLCJzdWIiOiIxMjM0MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MSwiZXhwIjoxNjA1ODA0OTcxfQ.8gfZVF17kBzHST-w4QkQugeJqA79BaJjkPJHJX2jopU"
```
# Reporting

Meeting Evaluation Reporting

## Average Number of Attendees


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/average_attendees?by_period[starts_at]=2020-10-25+16%3A56%3A09+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A09+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1ODdkN2IzNC01N2NkLTQxYmEtYTg4Zi1mNmQ4YWE2MTdhZmMiLCJzdWIiOiIxMjMyNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OSwiZXhwIjoxNjA1ODA0OTY5fQ.L3zupva_FSHQoxmUxoOc_ihpSFyHTCXuDKN_uVxNduU
```

`GET /api/v1/reporting/user/evaluations/average_attendees`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:09 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:09 UTC&quot;}
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
    "id": "b62d6eb9-ca7c-40ad-a690-56872fd97f1d",
    "type": "reports",
    "attributes": {
      "name": "Attendees",
      "starts_at": "2020-10-25T00:00:00.000Z",
      "ends_at": "2020-11-01T23:59:59.999Z",
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
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/average_attendees?by_period[starts_at]=2020-10-25+16%3A56%3A09+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A09+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1ODdkN2IzNC01N2NkLTQxYmEtYTg4Zi1mNmQ4YWE2MTdhZmMiLCJzdWIiOiIxMjMyNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OSwiZXhwIjoxNjA1ODA0OTY5fQ.L3zupva_FSHQoxmUxoOc_ihpSFyHTCXuDKN_uVxNduU"
```
## Average scores per evaluator


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/averages?by_period[starts_at]=2020-10-25+16%3A56%3A08+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A08+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjM2FmMzE1YS1mMDQxLTQwOWUtYWRmNC02ODljZTc2ZWVhMmEiLCJzdWIiOiIxMjMyNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.6NtnQaaJiAAXFV0ADx-Cjd7phygijyrKz4cpA2J-5Og
```

`GET /api/v1/reporting/user/evaluations/averages`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:08 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:08 UTC&quot;}
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
    "id": "ddbdc610-80c1-4fef-80a1-c90bc9aad54f",
    "type": "reports",
    "attributes": {
      "name": "Evaluation averages and totals",
      "starts_at": "2020-10-25T00:00:00.000Z",
      "ends_at": "2020-11-01T23:59:59.999Z",
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
        "quality_label": "What would make these meetings more effective?"
      },
      "trends": null,
      "average": 0.0,
      "total": 0.0
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/averages?by_period[starts_at]=2020-10-25+16%3A56%3A08+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A08+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJjM2FmMzE1YS1mMDQxLTQwOWUtYWRmNC02ODljZTc2ZWVhMmEiLCJzdWIiOiIxMjMyNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.6NtnQaaJiAAXFV0ADx-Cjd7phygijyrKz4cpA2J-5Og"
```
## Company User Counts


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/team/evaluations/user_counts?by_period[starts_at]=2020-10-25+16%3A56%3A10+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A10+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMDI2MDEyYi1mY2M4LTRjNTctOTZlYi01ZGUzNmZlMWI3MGEiLCJzdWIiOiIxMjM0MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MSwiZXhwIjoxNjA1ODA0OTcxfQ.9KR2M88SKzdSWTgCxqHwrmaCrDZDcC6hNDXOcLFieBk
```

`GET /api/v1/reporting/team/evaluations/user_counts`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:10 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:10 UTC&quot;}
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
    "id": "93fe03ba-f190-4066-9ffc-6a9c669bfb27",
    "type": "reports",
    "attributes": {
      "name": "Team User Count",
      "starts_at": "2020-10-25T00:00:00.000Z",
      "ends_at": "2020-11-01T23:59:59.999Z",
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
curl -g "http://localhost:3000/api/v1/reporting/team/evaluations/user_counts?by_period[starts_at]=2020-10-25+16%3A56%3A10+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A10+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMDI2MDEyYi1mY2M4LTRjNTctOTZlYi01ZGUzNmZlMWI3MGEiLCJzdWIiOiIxMjM0MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3MSwiZXhwIjoxNjA1ODA0OTcxfQ.9KR2M88SKzdSWTgCxqHwrmaCrDZDcC6hNDXOcLFieBk"
```
## Duration and Cost Details


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/duration_and_cost_details?by_period[starts_at]=2020-10-25+16%3A56%3A08+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A08+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3MmQ3ZTRjOC0wMDc2LTQ3MzQtODgyNi0zMWYxNWE4NTU2MTgiLCJzdWIiOiIxMjMyMSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.wKVmH0rLEb08bkmpUVS78mYnO1TILzVZrSTON1Dei-M
```

`GET /api/v1/reporting/user/evaluations/duration_and_cost_details`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:08 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:08 UTC&quot;}
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
    "id": "0fb81053-058c-4658-89be-783e0dfe88f3",
    "type": "reports",
    "attributes": {
      "name": "Duration and Costs Details",
      "starts_at": "2020-10-25T00:00:00.000Z",
      "ends_at": "2020-11-01T23:59:59.999Z",
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
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/duration_and_cost_details?by_period[starts_at]=2020-10-25+16%3A56%3A08+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A08+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3MmQ3ZTRjOC0wMDc2LTQ3MzQtODgyNi0zMWYxNWE4NTU2MTgiLCJzdWIiOiIxMjMyMSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.wKVmH0rLEb08bkmpUVS78mYnO1TILzVZrSTON1Dei-M"
```
## Duration and Costs


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/duration_and_costs?by_period[starts_at]=2020-10-25+16%3A56%3A08+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A08+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMThjYmFmZi00NTRkLTRhYTYtYTllMi1jZTQxNTJhZDY2NWQiLCJzdWIiOiIxMjMyMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.Gh6wfxWHjC4mTRC7mdE6uFadFNrAUhHhLKUttFEQKVA
```

`GET /api/v1/reporting/user/evaluations/duration_and_costs`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:08 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:08 UTC&quot;}
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
    "id": "f68d6d8a-6865-4b2d-b83f-1ebdf4e405d9",
    "type": "reports",
    "attributes": {
      "name": "Duration and Costs Summary",
      "starts_at": "2020-10-25T00:00:00.000Z",
      "ends_at": "2020-11-01T23:59:59.999Z",
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
          "work_hours": 40.0,
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
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/duration_and_costs?by_period[starts_at]=2020-10-25+16%3A56%3A08+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A08+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMThjYmFmZi00NTRkLTRhYTYtYTllMi1jZTQxNTJhZDY2NWQiLCJzdWIiOiIxMjMyMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.Gh6wfxWHjC4mTRC7mdE6uFadFNrAUhHhLKUttFEQKVA"
```
## Late Scheduled Meetings


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/scheduled_late?by_period[starts_at]=2020-10-25+16%3A56%3A08+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A08+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMmYzODcxOC0yNDAyLTRhMGMtOWRlNy1hMGUwMWUwZDkxMDgiLCJzdWIiOiIxMjMyNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OSwiZXhwIjoxNjA1ODA0OTY5fQ.mxTbU99L2g_FYzZvdfONWSCO6MuSaOp7UUTo8YCFWZA
```

`GET /api/v1/reporting/user/evaluations/scheduled_late`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:08 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:08 UTC&quot;}
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
    "id": "c2a2db9d-ceaa-486c-b882-6178aefd7ff7",
    "type": "reports",
    "attributes": {
      "name": "Scheduled late",
      "starts_at": "2020-10-25T00:00:00.000Z",
      "ends_at": "2020-11-01T23:59:59.999Z",
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
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/scheduled_late?by_period[starts_at]=2020-10-25+16%3A56%3A08+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A08+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhMmYzODcxOC0yNDAyLTRhMGMtOWRlNy1hMGUwMWUwZDkxMDgiLCJzdWIiOiIxMjMyNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OSwiZXhwIjoxNjA1ODA0OTY5fQ.mxTbU99L2g_FYzZvdfONWSCO6MuSaOp7UUTo8YCFWZA"
```
## Overtime Meeting Hours


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/overtime?by_period[starts_at]=2020-10-25+16%3A56%3A08+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A08+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxOWEwMjliMy02NjU3LTQ3NjEtODA3OC1jZTdlYmI4MDk2MGEiLCJzdWIiOiIxMjMyNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.qSnRYNvK05hn2bHMHYx4DMZ7HeneZQY3_3Swb20Uk2Q
```

`GET /api/v1/reporting/user/evaluations/overtime`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:08 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:08 UTC&quot;}
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
    "id": "0e401136-06bf-4a19-a59d-e9e468778168",
    "type": "reports",
    "attributes": {
      "name": "Overtime",
      "starts_at": "2020-10-25T00:00:00.000Z",
      "ends_at": "2020-11-01T23:59:59.999Z",
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
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/overtime?by_period[starts_at]=2020-10-25+16%3A56%3A08+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A08+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxOWEwMjliMy02NjU3LTQ3NjEtODA3OC1jZTdlYmI4MDk2MGEiLCJzdWIiOiIxMjMyNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.qSnRYNvK05hn2bHMHYx4DMZ7HeneZQY3_3Swb20Uk2Q"
```
## Wellness Block Conflicts


### Request

#### Endpoint

```plaintext
GET /api/v1/reporting/user/evaluations/focus_block_conflict?by_period[starts_at]=2020-10-25+16%3A56%3A08+UTC&amp;by_period[ends_at]=2020-11-01+16%3A56%3A08+UTC
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlMjcwMWRiMi1lMTRhLTQ2MTMtODJjZC0wNWYyODBlZWE1ZWUiLCJzdWIiOiIxMjMyMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.mHfdFz_PH2gBP5qx0ZdipxvWJIqzbkuGxEaNVMyloNY
```

`GET /api/v1/reporting/user/evaluations/focus_block_conflict`

#### Parameters


```json
by_period: {&quot;starts_at&quot;=&gt;&quot;2020-10-25 16:56:08 UTC&quot;, &quot;ends_at&quot;=&gt;&quot;2020-11-01 16:56:08 UTC&quot;}
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
    "id": "42821731-6f51-478f-a365-602b99231922",
    "type": "reports",
    "attributes": {
      "name": "Focus block conflict",
      "starts_at": "2020-10-25T00:00:00.000Z",
      "ends_at": "2020-11-01T23:59:59.999Z",
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
curl -g "http://localhost:3000/api/v1/reporting/user/evaluations/focus_block_conflict?by_period[starts_at]=2020-10-25+16%3A56%3A08+UTC&by_period[ends_at]=2020-11-01+16%3A56%3A08+UTC" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlMjcwMWRiMi1lMTRhLTQ2MTMtODJjZC0wNWYyODBlZWE1ZWUiLCJzdWIiOiIxMjMyMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2OCwiZXhwIjoxNjA1ODA0OTY4fQ.mHfdFz_PH2gBP5qx0ZdipxvWJIqzbkuGxEaNVMyloNY"
```
# Settings Labels



## List settings labels


### Request

#### Endpoint

```plaintext
GET /api/v1/settings_labels
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwYTJlMjdjOS0xODJmLTRkYTAtYWIyMi03N2IwODk5ZWUxNmQiLCJzdWIiOiIxMjI5NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NCwiZXhwIjoxNjA1ODA0OTY0fQ.yKgrnrBReSfb5XotI-W40HYxRg6LxWwW2vfqCtmoPBQ
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
    "id": "5e92a9f8-af83-4bae-8c1c-7e6d884bfdfe",
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwYTJlMjdjOS0xODJmLTRkYTAtYWIyMi03N2IwODk5ZWUxNmQiLCJzdWIiOiIxMjI5NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NCwiZXhwIjoxNjA1ODA0OTY0fQ.yKgrnrBReSfb5XotI-W40HYxRg6LxWwW2vfqCtmoPBQ"
```
# Stripe

Stripe Subscriptions

## Create Stripe Session


### Request

#### Endpoint

```plaintext
POST /api/v1/stripe_checkout/sessions
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyZGNlYTM5Ny1iNzQ2LTQwNjEtOTJjZi00MTU3ZDNlNTdhYTMiLCJzdWIiOiIxMjM4MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NywiZXhwIjoxNjA1ODA0OTc3fQ.97eY2ht-aFYiiTHAhmnDupB_6_GY1D47u7sC83VkdV8
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyZGNlYTM5Ny1iNzQ2LTQwNjEtOTJjZi00MTU3ZDNlNTdhYTMiLCJzdWIiOiIxMjM4MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NywiZXhwIjoxNjA1ODA0OTc3fQ.97eY2ht-aFYiiTHAhmnDupB_6_GY1D47u7sC83VkdV8"
```
## Delete Stripe Subscription


### Request

#### Endpoint

```plaintext
DELETE /api/v1/subscription
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyZDc1YWJmZC05MzI4LTQ2NDktODBiMC1hODg3NzdiMjA3NTYiLCJzdWIiOiIxMjI5MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NCwiZXhwIjoxNjA1ODA0OTY0fQ.29Q3E58qDqZD6NsuDuCYmxIeHcIxUAgx5hhHI4a4T3Y
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
    "id": "627",
    "type": "subscriptions",
    "attributes": {
      "stripe_id": "test_su_4",
      "active": false,
      "created_at": "2020-10-25T16:56:04.442Z",
      "current_period_start": "2020-10-25T16:56:04.000Z",
      "current_period_end": "2020-11-25T16:56:04.000Z",
      "amount": 438,
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyZDc1YWJmZC05MzI4LTQ2NDktODBiMC1hODg3NzdiMjA3NTYiLCJzdWIiOiIxMjI5MSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NCwiZXhwIjoxNjA1ODA0OTY0fQ.29Q3E58qDqZD6NsuDuCYmxIeHcIxUAgx5hhHI4a4T3Y"
```
## Update Stripe Session


### Request

#### Endpoint

```plaintext
PUT /api/v1/stripe_checkout/sessions
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwOWZiN2ZmNy1lMmIwLTQ2YTYtODM4OC05YzdhMzg2MjQ3MjQiLCJzdWIiOiIxMjM4MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NywiZXhwIjoxNjA1ODA0OTc3fQ.c-NG3XSwJ0GDF64l-bo80qA6j-1iZ4m2AiiPEZjkuy0
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwOWZiN2ZmNy1lMmIwLTQ2YTYtODM4OC05YzdhMzg2MjQ3MjQiLCJzdWIiOiIxMjM4MCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NywiZXhwIjoxNjA1ODA0OTc3fQ.c-NG3XSwJ0GDF64l-bo80qA6j-1iZ4m2AiiPEZjkuy0"
```
## Update Stripe Subscription


### Request

#### Endpoint

```plaintext
PUT /api/v1/subscription
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxZWQ4Yzk0Yy03MTBlLTQ0YWQtOWFhZi04MTc5ZGE4OTk1MDYiLCJzdWIiOiIxMjI5MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NCwiZXhwIjoxNjA1ODA0OTY0fQ.8s7dyXZPg-8SH-0flJRB1PQeLzx4HMyPD3W5ycvfj-4
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
    "id": "628",
    "type": "subscriptions",
    "attributes": {
      "stripe_id": "test_txn_default",
      "active": true,
      "created_at": "2020-10-25T16:56:04.604Z",
      "current_period_start": "2020-10-25T16:56:04.000Z",
      "current_period_end": "2020-11-25T16:56:04.000Z",
      "amount": 438,
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIxZWQ4Yzk0Yy03MTBlLTQ0YWQtOWFhZi04MTc5ZGE4OTk1MDYiLCJzdWIiOiIxMjI5MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NCwiZXhwIjoxNjA1ODA0OTY0fQ.8s7dyXZPg-8SH-0flJRB1PQeLzx4HMyPD3W5ycvfj-4"
```
# Subscription



## Show subscription


### Request

#### Endpoint

```plaintext
GET /api/v1/subscription
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlY2IyMThhMS0wYzc2LTQzM2ItODJjOS1kNmIyZTBmOGQwMWUiLCJzdWIiOiIxMjM4MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OCwiZXhwIjoxNjA1ODA0OTc4fQ.x_zH8whnCx1ndtZ5x6lMUCxT6fpTtX7xBK7o5Thkt7M
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
    "id": "635",
    "type": "subscriptions",
    "attributes": {
      "stripe_id": "tok_jcb",
      "active": true,
      "created_at": "2020-10-25T16:56:18.091Z",
      "current_period_start": null,
      "current_period_end": null,
      "amount": 438,
      "category": "user",
      "plan": "team-438",
      "product_id": "team-400"
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/subscription" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlY2IyMThhMS0wYzc2LTQzM2ItODJjOS1kNmIyZTBmOGQwMWUiLCJzdWIiOiIxMjM4MiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OCwiZXhwIjoxNjA1ODA0OTc4fQ.x_zH8whnCx1ndtZ5x6lMUCxT6fpTtX7xBK7o5Thkt7M"
```
# Subscription Plans



## List subscription plans


### Request

#### Endpoint

```plaintext
GET /api/v1/subscription_plans
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyODk1ZjdiZC03Y2MzLTQ3MmYtYmFjMC1jM2YzNWQ2YzZhOGYiLCJzdWIiOiIxMjI5MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NCwiZXhwIjoxNjA1ODA0OTY0fQ.iCZtBxSYmMCwtYphKT3spN2ZisXnefl_QbwIWpEXTr0
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyODk1ZjdiZC03Y2MzLTQ3MmYtYmFjMC1jM2YzNWQ2YzZhOGYiLCJzdWIiOiIxMjI5MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NCwiZXhwIjoxNjA1ODA0OTY0fQ.iCZtBxSYmMCwtYphKT3spN2ZisXnefl_QbwIWpEXTr0"
```
# Team Invites



## Create invite


### Request

#### Endpoint

```plaintext
POST /api/v1/invites
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyODBmNzg3NC0yZTdlLTQyMzItOTVkNS05NzU1YjUzNTY3YjAiLCJzdWIiOiIxMjI5OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NSwiZXhwIjoxNjA1ODA0OTY1fQ.sJkM94hH0MUX8KE60ph1r88MBSMqS8m9EVQXah47kFI
```

`POST /api/v1/invites`

#### Parameters


```json
{"data":{"type":"agenda_item","attributes":{"email":"theodore_treutel@lueilwitz.org"}}}
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
    "id": "94",
    "type": "invites",
    "attributes": {
      "team_id": 12594,
      "user_id": 12299,
      "email": "theodore_treutel@lueilwitz.org",
      "created_at": "2020-10-25T16:56:05.479Z",
      "accepted_at": "2020-10-25T16:56:05.538Z"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/invites" -d '{"data":{"type":"agenda_item","attributes":{"email":"theodore_treutel@lueilwitz.org"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyODBmNzg3NC0yZTdlLTQyMzItOTVkNS05NzU1YjUzNTY3YjAiLCJzdWIiOiIxMjI5OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NSwiZXhwIjoxNjA1ODA0OTY1fQ.sJkM94hH0MUX8KE60ph1r88MBSMqS8m9EVQXah47kFI"
```
## Delete invite


### Request

#### Endpoint

```plaintext
DELETE /api/v1/invites/93
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3YWMxZDNkMi05OGFlLTRjZmYtOWE5Yy1lYzU0ZDlhZTAwMDQiLCJzdWIiOiIxMjI5NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NSwiZXhwIjoxNjA1ODA0OTY1fQ.JS9_f450sJoJCzDgCwtRq_XZehQigEHkFu0PU_Vs4Lw
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
curl "http://localhost:3000/api/v1/invites/93" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI3YWMxZDNkMi05OGFlLTRjZmYtOWE5Yy1lYzU0ZDlhZTAwMDQiLCJzdWIiOiIxMjI5NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NSwiZXhwIjoxNjA1ODA0OTY1fQ.JS9_f450sJoJCzDgCwtRq_XZehQigEHkFu0PU_Vs4Lw"
```
## List invites


### Request

#### Endpoint

```plaintext
GET /api/v1/invites
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNTNmOGM2MC1iNjdhLTRiNzQtYTk4NS00ODhiZGI4MDVjMzUiLCJzdWIiOiIxMjI5NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NSwiZXhwIjoxNjA1ODA0OTY1fQ.sldak4GVbMsw9DWoXB0m1ajTuAdxfb74jjTbPEfOrkc
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNTNmOGM2MC1iNjdhLTRiNzQtYTk4NS00ODhiZGI4MDVjMzUiLCJzdWIiOiIxMjI5NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NSwiZXhwIjoxNjA1ODA0OTY1fQ.sldak4GVbMsw9DWoXB0m1ajTuAdxfb74jjTbPEfOrkc"
```
# Team Members



## Add membership to team


### Request

#### Endpoint

```plaintext
POST /api/v1/teams/12599/members
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYTM2YzY5Mi1lNjg3LTRhMzAtODU0OS02MTQ2MTUzMGU3YTkiLCJzdWIiOiIxMjMwMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NiwiZXhwIjoxNjA1ODA0OTY2fQ.lKXEdGjdywf4NxRn5MYFwwJs7qf9Oz4yjhBoF83ckwg
```

`POST /api/v1/teams/:id/members`

#### Parameters


```json
{"data":{"type":"team","attributes":{"user_id":12305,"role":"billing_admin"}}}
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
    "id": "12482",
    "type": "memberships",
    "attributes": {
      "user_id": 12305,
      "role": "billing_admin",
      "name": "Giant Phoenix Cheetah XI",
      "email": "test2@test.com",
      "licensed": false,
      "profile_image": "http://effertz.co/cristobal.cummings"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/teams/12599/members" -d '{"data":{"type":"team","attributes":{"user_id":12305,"role":"billing_admin"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiYTM2YzY5Mi1lNjg3LTRhMzAtODU0OS02MTQ2MTUzMGU3YTkiLCJzdWIiOiIxMjMwMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NiwiZXhwIjoxNjA1ODA0OTY2fQ.lKXEdGjdywf4NxRn5MYFwwJs7qf9Oz4yjhBoF83ckwg"
```
## Delete membership


### Request

#### Endpoint

```plaintext
DELETE /api/v1/teams/12605/members/12491
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0MTcwOGM3Ny1kOTFkLTRlZDYtYmQ5OC1hOTcxMmVjNzM0YjMiLCJzdWIiOiIxMjMxMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NiwiZXhwIjoxNjA1ODA0OTY2fQ.ywgDGkVwTQ9VLBT7mTST5pU-Ak5l_WBELJEV1b4ZltQ
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
curl "http://localhost:3000/api/v1/teams/12605/members/12491" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI0MTcwOGM3Ny1kOTFkLTRlZDYtYmQ5OC1hOTcxMmVjNzM0YjMiLCJzdWIiOiIxMjMxMCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NiwiZXhwIjoxNjA1ODA0OTY2fQ.ywgDGkVwTQ9VLBT7mTST5pU-Ak5l_WBELJEV1b4ZltQ"
```
## List team memberships


### Request

#### Endpoint

```plaintext
GET /api/v1/teams/12601/members
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwNTc0YmNiMC02ODMyLTQwZWMtOTAyNC01MDQxYjdkOTM1MjkiLCJzdWIiOiIxMjMwNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NiwiZXhwIjoxNjA1ODA0OTY2fQ.YjqLSzML_JBo9vqecjc3NcO6y5LcdNi8pxLwePfLv60
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
      "id": "12483",
      "type": "memberships",
      "attributes": {
        "user_id": 12306,
        "role": "billing_admin",
        "name": "General Ripcord Magnificent Hercules",
        "email": "rich@kris.name",
        "licensed": true,
        "profile_image": "http://moen-gleichner.net/valentina.muller"
      }
    },
    {
      "id": "12485",
      "type": "memberships",
      "attributes": {
        "user_id": 12307,
        "role": "billing_admin",
        "name": "Doctor Synch the Hunter Cable XI",
        "email": "test1@test.com",
        "licensed": true,
        "profile_image": "http://mante-gutmann.biz/nohemi_carroll"
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
curl -g "http://localhost:3000/api/v1/teams/12601/members" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwNTc0YmNiMC02ODMyLTQwZWMtOTAyNC01MDQxYjdkOTM1MjkiLCJzdWIiOiIxMjMwNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NiwiZXhwIjoxNjA1ODA0OTY2fQ.YjqLSzML_JBo9vqecjc3NcO6y5LcdNi8pxLwePfLv60"
```
## Update membership


### Request

#### Endpoint

```plaintext
PUT /api/v1/teams/12603/members/12488
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwNDEyYzIyYS01ZDA5LTQzZjMtOWZlYi00NWQ5NDNmZWY0NTIiLCJzdWIiOiIxMjMwOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NiwiZXhwIjoxNjA1ODA0OTY2fQ.cREP0WPaHhPW6M1JWcWFyQxYqX0AgCSrSOb7FHFHz_w
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
    "id": "12488",
    "type": "memberships",
    "attributes": {
      "user_id": 12309,
      "role": "billing_admin",
      "name": "Ultron I Osiris Machine",
      "email": "test1@test.com",
      "licensed": true,
      "profile_image": "http://nikolaus.net/jade"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/teams/12603/members/12488" -d '{"data":{"type":"team","attributes":{"role":"billing_admin","licensed":true}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIwNDEyYzIyYS01ZDA5LTQzZjMtOWZlYi00NWQ5NDNmZWY0NTIiLCJzdWIiOiIxMjMwOCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2NiwiZXhwIjoxNjA1ODA0OTY2fQ.cREP0WPaHhPW6M1JWcWFyQxYqX0AgCSrSOb7FHFHz_w"
```
# Teams

Update team attributes or evaluation settings

## List teams


### Request

#### Endpoint

```plaintext
GET /api/v1/teams
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2Nzc2NTliNy0wMTBjLTRiNjUtYTdjZS0yNDVmZGYyNjhiN2YiLCJzdWIiOiIxMjM4NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OCwiZXhwIjoxNjA1ODA0OTc4fQ.iOefMk59MI0nFJGWMpdVNvf6_vLEdllV-05qS_9Paos
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
      "id": "12683",
      "type": "teams",
      "attributes": {
        "name": "ruecker",
        "image": null,
        "domain": "ruecker.co",
        "license_by": "domain",
        "current_user_membership": {
          "id": 12566,
          "user_id": 12386,
          "created_at": "2020-10-25T16:56:18.591Z",
          "updated_at": "2020-10-25T16:56:18.591Z",
          "role": "billing_admin",
          "team_id": 12683,
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2Nzc2NTliNy0wMTBjLTRiNjUtYTdjZS0yNDVmZGYyNjhiN2YiLCJzdWIiOiIxMjM4NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OCwiZXhwIjoxNjA1ODA0OTc4fQ.iOefMk59MI0nFJGWMpdVNvf6_vLEdllV-05qS_9Paos"
```
## Show team


### Request

#### Endpoint

```plaintext
GET /api/v1/teams/12682
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhOTFhYTYzZi1hYmFjLTRlNjMtOGI0Ni04MjMyMTNmZmI3NTMiLCJzdWIiOiIxMjM4NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OCwiZXhwIjoxNjA1ODA0OTc4fQ.RUXZCE7aL9766uHFCKMiqojGG9cg_7hgZ6zIBWtokcw
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
    "id": "12682",
    "type": "teams",
    "attributes": {
      "name": "powlowski",
      "image": null,
      "domain": "powlowski.net",
      "license_by": "domain",
      "current_user_membership": {
        "id": 12565,
        "user_id": 12385,
        "created_at": "2020-10-25T16:56:18.459Z",
        "updated_at": "2020-10-25T16:56:18.459Z",
        "role": "billing_admin",
        "team_id": 12682,
        "licensed": true
      }
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/teams/12682" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJhOTFhYTYzZi1hYmFjLTRlNjMtOGI0Ni04MjMyMTNmZmI3NTMiLCJzdWIiOiIxMjM4NSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OCwiZXhwIjoxNjA1ODA0OTc4fQ.RUXZCE7aL9766uHFCKMiqojGG9cg_7hgZ6zIBWtokcw"
```
## Update team


### Request

#### Endpoint

```plaintext
PUT /api/v1/teams/12681
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNmVkNDBhZi04MmFiLTQ0MTctOGQ3ZC1jZmNhMTI0YTNmZGMiLCJzdWIiOiIxMjM4NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OCwiZXhwIjoxNjA1ODA0OTc4fQ.OHaAsADmZs2rnShau5EbHQamcimdNe4nBVBPvBtFfCE
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
    "id": "12681",
    "type": "teams",
    "attributes": {
      "name": "grady-fadel",
      "image": null,
      "domain": "grady-fadel.io",
      "license_by": "invite",
      "current_user_membership": {
        "id": 12564,
        "user_id": 12384,
        "created_at": "2020-10-25T16:56:18.311Z",
        "updated_at": "2020-10-25T16:56:18.311Z",
        "role": "billing_admin",
        "team_id": 12681,
        "licensed": true
      }
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/teams/12681" -d '{"data":{"type":"team","attributes":{"required_category":true,"required_agenda":true,"license_by":"invite","annual_salary":220000}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyNmVkNDBhZi04MmFiLTQ0MTctOGQ3ZC1jZmNhMTI0YTNmZGMiLCJzdWIiOiIxMjM4NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3OCwiZXhwIjoxNjA1ODA0OTc4fQ.OHaAsADmZs2rnShau5EbHQamcimdNe4nBVBPvBtFfCE"
```
# Tips



## Clear all tips for user


### Request

#### Endpoint

```plaintext
DELETE /api/v1/tips/all
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1NzA0ZDkzOS1hZDhlLTRhYmQtOWVkYS02ZTA0YzYxNWYyY2EiLCJzdWIiOiIxMjI3NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MiwiZXhwIjoxNjA1ODA0OTYyfQ.-pSmnDwG6IwVh2bIWTlsH490wNBMn5IS3FT-wwgNVw0
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI1NzA0ZDkzOS1hZDhlLTRhYmQtOWVkYS02ZTA0YzYxNWYyY2EiLCJzdWIiOiIxMjI3NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MiwiZXhwIjoxNjA1ODA0OTYyfQ.-pSmnDwG6IwVh2bIWTlsH490wNBMn5IS3FT-wwgNVw0"
```
## Flag tip as seen for user


### Request

#### Endpoint

```plaintext
PUT /api/v1/tips/5
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNjRjNzVmOC1kMzBkLTQ2OTYtYjA5OS04ODQ5MmE1YjE3ZmEiLCJzdWIiOiIxMjI3NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MiwiZXhwIjoxNjA1ODA0OTYyfQ.5jG8HKoUj1cCGc2_wwXahUAge8g-6CeUk6RqzocyO6I
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
      "seen_at": "2020-10-25T16:56:02.275Z"
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/tips/5" -d '' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJiNjRjNzVmOC1kMzBkLTQ2OTYtYjA5OS04ODQ5MmE1YjE3ZmEiLCJzdWIiOiIxMjI3NiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MiwiZXhwIjoxNjA1ODA0OTYyfQ.5jG8HKoUj1cCGc2_wwXahUAge8g-6CeUk6RqzocyO6I"
```
## List tips for user


### Request

#### Endpoint

```plaintext
GET /api/v1/tips
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzODEwNjVkYS1lMWY4LTRkYjUtOTE4YS1kOWUwNDcwMjAyZmUiLCJzdWIiOiIxMjI3OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MiwiZXhwIjoxNjA1ODA0OTYyfQ.vXi9Ki-IBbiKwUKKrTImgX18_zi18vjBUn34t3EwMwQ
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIzODEwNjVkYS1lMWY4LTRkYjUtOTE4YS1kOWUwNDcwMjAyZmUiLCJzdWIiOiIxMjI3OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MiwiZXhwIjoxNjA1ODA0OTYyfQ.vXi9Ki-IBbiKwUKKrTImgX18_zi18vjBUn34t3EwMwQ"
```
# Users

Update user action or evaluation settings

## Delete user account and all associated data


### Request

#### Endpoint

```plaintext
DELETE /api/v1/users
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlNGU3MjJmNS04OGFjLTQxMTctYjUzYi01ZjU0OTFjYmQxNjMiLCJzdWIiOiIxMjM1OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NCwiZXhwIjoxNjA1ODA0OTc0fQ.p6FLhkBbNM3sqxz2cffdKuXR9p8uG1kihlhOJha9KUM
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlNGU3MjJmNS04OGFjLTQxMTctYjUzYi01ZjU0OTFjYmQxNjMiLCJzdWIiOiIxMjM1OSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NCwiZXhwIjoxNjA1ODA0OTc0fQ.p6FLhkBbNM3sqxz2cffdKuXR9p8uG1kihlhOJha9KUM"
```
## Show user


### Request

#### Endpoint

```plaintext
GET /api/v1/users
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2ZjZlNWNjYi1jZTBjLTQzMDAtYWY2Mi0yOTJhZjEzNTJkNGUiLCJzdWIiOiIxMjM1OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NCwiZXhwIjoxNjA1ODA0OTc0fQ.VZFpQBDN19XUhr6iQ3SfntxwFYe3c8J7Vc_hq3SdurY
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
    "id": "12358",
    "type": "users",
    "attributes": {
      "email": "billy@weimann-larkin.org",
      "domain": "weimann-larkin.org",
      "first_name": "Crystal Dragon",
      "last_name": "Ajax Lord",
      "profile_image": "http://kreiger.biz/orval_kilback",
      "time_zone": "UTC",
      "onboarded": false,
      "identity_providers": [

      ],
      "subscription_plan": null,
      "daily_report_card_events": true,
      "company": {
        "id": 12653,
        "name": "weimann-larkin",
        "license_by": "domain",
        "roles": [
          "billing_admin"
        ]
      },
      "organizer_blacklist": "",
      "domain_whitelist": "weimann-larkin.org",
      "communication_prefs": {
        "all_communications": true,
        "email_tips": true,
        "email_weekly_reports": true,
        "email_reminders": true
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI2ZjZlNWNjYi1jZTBjLTQzMDAtYWY2Mi0yOTJhZjEzNTJkNGUiLCJzdWIiOiIxMjM1OCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NCwiZXhwIjoxNjA1ODA0OTc0fQ.VZFpQBDN19XUhr6iQ3SfntxwFYe3c8J7Vc_hq3SdurY"
```
## Show user settings


### Request

#### Endpoint

```plaintext
GET /api/v1/users/settings
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMzNlN2EwNy02NjQxLTRlYjEtOWMwZC1hNzNmZGQ3MGI1ZGYiLCJzdWIiOiIxMjI3NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MSwiZXhwIjoxNjA1ODA0OTYxfQ.prbfZsieumHYPpdPFlipBpMZVCJEc1kFjE-9qj7YhcQ
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
    "id": "12274",
    "type": "user_settings",
    "attributes": {
      "action_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "non_compliance_action": "remind",
        "domains_whitelist": "smith.org",
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkMzNlN2EwNy02NjQxLTRlYjEtOWMwZC1hNzNmZGQ3MGI1ZGYiLCJzdWIiOiIxMjI3NCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MSwiZXhwIjoxNjA1ODA0OTYxfQ.prbfZsieumHYPpdPFlipBpMZVCJEc1kFjE-9qj7YhcQ"
```
## Update user


### Request

#### Endpoint

```plaintext
PUT /api/v1/users
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkOTZlMzNiNS0wYmE3LTRiZTQtOTkzMC1mYWFiNGNiNDg5ZTMiLCJzdWIiOiIxMjM1NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NCwiZXhwIjoxNjA1ODA0OTc0fQ.1PpA1AtpYYBFdw5_C0sPG-7R9SGAHmwmwPMzHGCCq6o
```

`PUT /api/v1/users`

#### Parameters


```json
{"data":{"type":"team","attributes":{"required_category":true,"required_agenda":true,"annual_salary":220000}}}
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
    "id": "12357",
    "type": "users",
    "attributes": {
      "email": "geoffrey_beatty@vonrueden.name",
      "domain": "vonrueden.name",
      "first_name": "Supah Omega Red XI",
      "last_name": "Agent Callisto the Fated",
      "profile_image": "http://deckow.org/tanner",
      "time_zone": "UTC",
      "onboarded": false,
      "identity_providers": [

      ],
      "subscription_plan": null,
      "daily_report_card_events": true,
      "company": {
        "id": 12652,
        "name": "vonrueden",
        "license_by": "domain",
        "roles": [
          "billing_admin"
        ]
      },
      "organizer_blacklist": "",
      "domain_whitelist": "vonrueden.name",
      "communication_prefs": {
        "all_communications": true,
        "email_tips": true,
        "email_weekly_reports": true,
        "email_reminders": true
      },
      "goal_ids": [

      ]
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/users" -d '{"data":{"type":"team","attributes":{"required_category":true,"required_agenda":true,"annual_salary":220000}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkOTZlMzNiNS0wYmE3LTRiZTQtOTkzMC1mYWFiNGNiNDg5ZTMiLCJzdWIiOiIxMjM1NyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk3NCwiZXhwIjoxNjA1ODA0OTc0fQ.1PpA1AtpYYBFdw5_C0sPG-7R9SGAHmwmwPMzHGCCq6o"
```
## Update user settings


### Request

#### Endpoint

```plaintext
PUT /api/v1/users/settings
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlY2Q0NjFiYS1mZWJiLTQ0MDQtOGI3NC0wYmI0NTM5NDY2ZGIiLCJzdWIiOiIxMjI3MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MSwiZXhwIjoxNjA1ODA0OTYxfQ.MUHZNK-KjNERLLkefcjxTFDz7DKmRrSZ1LidbwXXlwo
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
    "id": "12273",
    "type": "user_settings",
    "attributes": {
      "action_settings": {
        "meeting_conflict": "block",
        "focus_block_conflict": "block",
        "non_compliance_action": "remind",
        "domains_whitelist": "lesch.net",
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlY2Q0NjFiYS1mZWJiLTQ0MDQtOGI3NC0wYmI0NTM5NDY2ZGIiLCJzdWIiOiIxMjI3MyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk2MSwiZXhwIjoxNjA1ODA0OTYxfQ.MUHZNK-KjNERLLkefcjxTFDz7DKmRrSZ1LidbwXXlwo"
```
# Wellness Blocks



## Create focus block


### Request

#### Endpoint

```plaintext
POST /api/v1/focus_blocks
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NzViMmRkNi0yNjJjLTQ0YjQtOTJlNC0zYmRhMzFjMmM4NDIiLCJzdWIiOiIxMjQwNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.NunaVAx0z6jMnfq4r9mDfy_vvngqQ3xa8yv1788BX4A
```

`POST /api/v1/focus_blocks`

#### Parameters


```json
{"data":{"type":"focus_block","attributes":{"label":"Coding MeetWell","calendar_id":14142,"rrule":"DTSTART;TZID=PST:20191228T140357\nRRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA","starts_at":"2019-12-28 22:03:57 UTC","ends_at":"2019-12-28 23:03:57 UTC"}}}
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
    "id": "460",
    "type": "focus_blocks",
    "attributes": {
      "label": "Coding MeetWell",
      "category": "focus",
      "calendar_id": 14142,
      "recurring_meeting_uuid": null,
      "duration": 3600,
      "starts_at": "2020-10-19T22:03:00.000Z",
      "ends_at": "2020-10-19T23:03:00.000Z",
      "rrule": "RRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA",
      "recurring": true
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/focus_blocks" -d '{"data":{"type":"focus_block","attributes":{"label":"Coding MeetWell","calendar_id":14142,"rrule":"DTSTART;TZID=PST:20191228T140357\nRRULE:FREQ=WEEKLY;BYDAY=MO,TU,WE,FR,SA","starts_at":"2019-12-28 22:03:57 UTC","ends_at":"2019-12-28 23:03:57 UTC"}}}' -X POST \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4NzViMmRkNi0yNjJjLTQ0YjQtOTJlNC0zYmRhMzFjMmM4NDIiLCJzdWIiOiIxMjQwNyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.NunaVAx0z6jMnfq4r9mDfy_vvngqQ3xa8yv1788BX4A"
```
## Delete wellness block


### Request

#### Endpoint

```plaintext
DELETE /api/v1/focus_blocks/458
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkZjE1OThlNC1hMGVhLTRhNDItYjNhZi0xZjdmNzhmN2Q5MGQiLCJzdWIiOiIxMjQwNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.abpxAvHpgfywgpuVjN81Gu2LykRFc-A-7K-QJWLeuIU
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
curl "http://localhost:3000/api/v1/focus_blocks/458" -d '' -X DELETE \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkZjE1OThlNC1hMGVhLTRhNDItYjNhZi0xZjdmNzhmN2Q5MGQiLCJzdWIiOiIxMjQwNSIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.abpxAvHpgfywgpuVjN81Gu2LykRFc-A-7K-QJWLeuIU"
```
## List maybe wellness blocks


### Request

#### Endpoint

```plaintext
GET /api/v1/focus_blocks/maybe
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4ZGRjYTkwZC04OTU2LTQzMTItYjA1ZS05Y2ZiYzg3N2ZiZTMiLCJzdWIiOiIxMjQwNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.7td8lIyQ5EgW2WRkfenqkOkgqJXrZLyruuQi2_rTGHM
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiI4ZGRjYTkwZC04OTU2LTQzMTItYjA1ZS05Y2ZiYzg3N2ZiZTMiLCJzdWIiOiIxMjQwNCIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.7td8lIyQ5EgW2WRkfenqkOkgqJXrZLyruuQi2_rTGHM"
```
## List wellness blocks


### Request

#### Endpoint

```plaintext
GET /api/v1/focus_blocks
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkN2U4OTg5Yi1iZjQ0LTRhMTItOTg5Ni04NGQ1ZjY4YTY5Y2IiLCJzdWIiOiIxMjQwNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.5_PPc0VQh8la63OV7WHLHYHvvt2DPTIvxV6AkwZ1EBU
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
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJkN2U4OTg5Yi1iZjQ0LTRhMTItOTg5Ni04NGQ1ZjY4YTY5Y2IiLCJzdWIiOiIxMjQwNiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.5_PPc0VQh8la63OV7WHLHYHvvt2DPTIvxV6AkwZ1EBU"
```
## Show wellness blocks


### Request

#### Endpoint

```plaintext
GET /api/v1/focus_blocks/457
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyM2RjNzE0NS00OThmLTQ3YWUtOWZlNy02NDExNTdhZmNkZWQiLCJzdWIiOiIxMjQwMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.b6hzKuH52uxrD1rYIG9mPed_ODnl0QOQTff5INbmII0
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
    "id": "457",
    "type": "focus_blocks",
    "attributes": {
      "label": "test",
      "category": "focus",
      "calendar_id": 14138,
      "recurring_meeting_uuid": "foo",
      "duration": 3600,
      "starts_at": "2020-10-25T16:56:00.000Z",
      "ends_at": "2020-10-25T17:56:00.000Z",
      "rrule": "RRULE:FREQ=DAILY",
      "recurring": true
    }
  }
}
```



```shell
curl -g "http://localhost:3000/api/v1/focus_blocks/457" -X GET \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiIyM2RjNzE0NS00OThmLTQ3YWUtOWZlNy02NDExNTdhZmNkZWQiLCJzdWIiOiIxMjQwMyIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.b6hzKuH52uxrD1rYIG9mPed_ODnl0QOQTff5INbmII0"
```
## Update wellness block


### Request

#### Endpoint

```plaintext
PUT /api/v1/focus_blocks/456
Content-Type: application/vnd.api+json
Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlOWYwZTJhYi0wNTMzLTQ4ZmItODY3ZS1iMWZhOWU5Zjc0MTEiLCJzdWIiOiIxMjQwMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.n-1PIrdK_A53a662LYFX4lKdX34oy1q15swqhxZH6pM
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
    "id": "456",
    "type": "focus_blocks",
    "attributes": {
      "label": "test",
      "category": "focus",
      "calendar_id": 14137,
      "recurring_meeting_uuid": "foo",
      "duration": 3600,
      "starts_at": "2020-10-23T16:56:00.000Z",
      "ends_at": "2020-10-23T17:56:00.000Z",
      "rrule": "RRULE:FREQ=WEEKLY;BYDAY=FR,SA",
      "recurring": true
    }
  }
}
```



```shell
curl "http://localhost:3000/api/v1/focus_blocks/456" -d '{"data":{"type":"focus_block","attributes":{"label":"test","rrule":"DTSTART;TZID=PST:20191228T140357\nRRULE:FREQ=WEEKLY;BYDAY=FR,SA","duration":3600}}}' -X PUT \
	-H "Content-Type: application/vnd.api+json" \
	-H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJqdGkiOiJlOWYwZTJhYi0wNTMzLTQ4ZmItODY3ZS1iMWZhOWU5Zjc0MTEiLCJzdWIiOiIxMjQwMiIsInNjcCI6InVzZXIiLCJhdWQiOm51bGwsImlhdCI6MTYwMzY0NDk4MSwiZXhwIjoxNjA1ODA0OTgxfQ.n-1PIrdK_A53a662LYFX4lKdX34oy1q15swqhxZH6pM"
```
