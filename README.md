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

# PicTweet_v6

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|email|string|null: false|
|username|string|null: false|
|password|string|null: false|
### Association
- has_many :posts

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false, foreign_key: true|
|group_name|string|null: false, foreign_key: true|
|member_id|integer|null: false, foreign_key: true|
|member_name|string|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## postsテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|image|???|???|

### Association
- belongs_to :user
- has_many :group