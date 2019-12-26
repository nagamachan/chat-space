# README
## usersテーブル

|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|name|string|null: false|

### Association
- has_many :groups
- has_many :messages
## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|

### Association
- has_many :users
-  has_many :messages
- has_many :groups_users
## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user|integer|null: false, foreign_key: true|
|group|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user
## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|body|text|-------|
|image|string|------|
|user|integer|null: false, foreign_key: true|
|group|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group
