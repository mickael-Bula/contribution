TABLE COMMENT
| champ        | type     | spécificité                                     | description          |
| ------------ | -------- | ----------------------------------------------- | -------------------- |
| code_comment | tiny int | Primary Key, Unsigned, NOT NULL, Auto Increment | comment's identifier |
| content      | text     | NOT NULL                                        | comment's content    |

TABLE USER
| champ     | type     | spécificité                                     | description       |
| --------- | -------- | ----------------------------------------------- | ----------------- |
| code_user | tiny int | Primary Key, Unsigned, NOT NULL, Auto Increment | user's identifier |
| username  | string   | NOT NULL                                        | user's username   |
| email     | string   | NOT NULL                                        | user's email      |
| roles     | string   | DEFAULT ['ROLE_USER']                           | user's roles      |

TABLE ADDRESS
| champ        | type     | spécificité                                     | description                |
| ------------ | -------- | ----------------------------------------------- | -------------------------- |
| code_address | tiny int | Primary Key, Unsigned, NOT NULL, Auto Increment | address' code              |
| street       | text     |                                                 | street in the address      |
| city         | string   | NOT NULL                                        | city in the address        |
| postal_code  | INT      | NOT NULL                                        | postal_code of the address |
|              |          |                                                 |                            |

TABLE EVENT
| champ       | type     | spécificité                                     | description         |
| ----------- | -------- | ----------------------------------------------- | ------------------- |
| code_event  | tiny int | Primary Key, Unsigned, NOT NULL, Auto Increment | address' code       |
| description | text     |                                                 | event's description |
| image       | string   |                                                 | event's image url   |
| start_date  | DATETIME |                                                 | event's start date  |
| end_date    | DATETIME |                                                 | event's end date    |

TABLE CATEGORY
| champ         | type     | spécificité                                     | description     |
| ------------- | -------- | ----------------------------------------------- | --------------- |
| code_category | tiny int | Primary Key, Unsigned, NOT NULL, Auto Increment | category's code |
| category_name | string   | NOT NULL                                        | category's name |

TABLE TAG
| champ    | type     | spécificité                                     | description       |
| -------- | -------- | ----------------------------------------------- | ----------------- |
| code_tag | tiny int | Primary Key, Unsigned, NOT NULL, Auto Increment | tag's code        |
| tag_name | string   | NOT NULL                                        | tag's description |
|          |          |                                                 |                   |
