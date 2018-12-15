## userテーブル
|Colum|Type|Options|
|-----|----|-------|
|user_id|integer|null: false, foreign_key:true|
|mail_add|string|null: false, foreign_key:true|

###Association

- has_many :group
- has_many :member
- has_many :chat

## groupテーブル
|Colim|Type|Options|
|-----|----|-------|
|user_id|integer|null: false, foreign_key:true|
|group_id|integer|null: false, foreign_key:true|

### Association
- belongs_to :user
- belongs_to :member
- has_many :chat


## membersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## chatテーブル
|Colum|Type|Options|
|-----|----|-------|
|user_id|integer|null: false, foreign_key:true|
|img|integer|

## Association
- has_many :user
- has_many :group
- has_many :member
kkkkk