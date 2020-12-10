# README

## usersテーブル

| Column     | Type   | Options     |
| ---------- | ------ | ----------- |
| email      | string | null: false |
| password   | string | null: false |
| name       | string | null: false |
| profile    | text   | null: false |
| occupation | text   | null: false |
| position   | text   | null: false |

### Association
- has_many :prototypes テーブル
- has_many :comments テーブル

## prototypesテーブル

| Column     | Type       | Options     |
| ---------- | ---------- | ----------- |
| title      | string     | null: false |
| catch_copy | text       | null: false |
| concept    | text       | null: false |
| user       | references |             |


### Association
- belongs_to :usersテーブル
- has_many :commentsテーブル

## commentsテーブル

| Column    | Type       | Options     |
| --------- | ---------- | ----------- |
| text      | text       | null: false |
| user      | references |             | 
| prototype | references |             |

### Association
- belongs_to :usersテーブル
- belongs_to :prototypesテーブル