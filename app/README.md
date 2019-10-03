## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer|null :false|
|text|text|null :false|
|image|string|text|||f
|user_id|integer|null: false, foreign_key: true|
 ### Association
 - belongs_to :user
 - belongs_to :group

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer|null:false,foreign_key: ture|
|member_id|integer|null :false|
### Association
- has_many :massages
- has_many :members

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|id|inter|
|email|string|null: false|
|password|string|null: false|
|group_id|null: true|
### Association
- has_many :messages
- has_many :groups through members
- has_many :members

## membersテーブル
|column|Type|Options|
|------|----|-------|
|group_id|integer|null :false|
|user_id|integer|null :false|
### Associationテーブル
- belongs_to :user


