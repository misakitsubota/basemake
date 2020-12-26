# README

## users table

| Column                | Type    | Options     |
| --------------------- | ------- | ----------- |
| nickname              | string  | null: false |
| email                 | string  | null: false |
| encrypted_password    | string  | null: false |

### Association
- has_many :items
- has_many :comments


## items table

| Column                | Type    | Options     |
| --------------------- | ------- | ----------- |
| image                 | string  | null: false |
| item_name             | string  | null: false |
| cost                  | integer | null: false |
| user_id               | integer | null: false, foreign_key: true |
| brand_id              | integer | null: false, foreign_key: true |
| category_id           | integer | null: false, foreign_key: true |


### Association
- belongs_to :user
- has_many :comments


## comments table

| Column               | Type    | Options     |
| ---------------      | ------- | ----------- |
| image                | string  | null: false |
| recommend_item_name  | string  | null: false |
| cost                 | integer | null: false |
| description          | text    | null: false |
| user_id              | integer | null: false, foreign_key: true |
| item_id              | integer | null: false, foreign_key: true |
| brand_id             | integer | null: false, foreign_key: true |
| category_id          | integer | null: false, foreign_key: true |


### Association
- belongs_to :user
- belongs_to :item





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
