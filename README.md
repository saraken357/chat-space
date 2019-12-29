# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


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


## group_usersテーブル

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
