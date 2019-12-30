## userテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|interger|foreign_key: true|
|name|varchar|null: false|
|Email|varchar|null: false|
|Password|varchar|null: false|

### Assosiation
- has_many :groups_users
- has_many :messages


## gruopテーブル

|Column|Type|Options|
|------|----|-------|
|group_id|interger|foreign_key: true|
|group_name|varchar|null: false|
|name|varchar|null: false, index: true|

### Assosiation
- has_many :groups_users
- has_many :messages


## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|interger|null: false, foreign_key: true|
|group_id|interger|null:false, foreign_key: ture|

### Assosiation
- belongs_to :group
- belongs_to :user


## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|body|text||
|image|string||
|group_id|interger|foreign_key: ture|
|users_id|interger|foreign_key: ture|

### Assosiation
- belongs_to :group
- belongs_to :user
