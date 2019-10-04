## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer||
|text|text||
|image|string||
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user
- belongs_to :group
## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer|null:false,foreign_key: ture|
|name|string|null: false|
### Association
- has_many :members
- has_many :messages
- has_many :users through members
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer|null: false|
|email|string|null: false|
|password|string|null: false|
|name|string|null: false|
### Association
- has_many :messages
- has_many :groups through members
- has_many :members
## membersテーブル
|column|Type|Options|
|------|----|-------|
|id|integer|null :false|
|group_id|integer|null :false|
|user_id|integer|null :false|
### Associationテーブル
- belongs_to :user
- belongs_to :group
