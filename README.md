## userテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|Email|varchar|null: false|
|Password|varchar|null: false|

### Assosiation
- has_many :groups, through: :groups_users
- has_many :groups_users
- has_many :messages


## groupテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false, index: true|

### Assosiation
- has_many :users, through: :groups_users
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
|group_id|interger|null: false, foreign_key: ture|
|user_id|interger|null: false, foreign_key: ture|

### Assosiation
- belongs_to :group
- belongs_to :user
