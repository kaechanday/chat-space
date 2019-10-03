## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer|null :false|
|text|text|null :false|
|image|string||
|user_id|integer|null: false|
|message_id|integer|null: false|
 ### Association
 - belongs_to :user
 - belongs_to :group

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer|null:false,foreign_key: ture|
### Association
- has_many :members

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer|
|email|string|null: false|
|password|string|null: false|
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
- belongs_to :user


