
# Attention! not for production
## sql deta

this mixin wraps just a few [Peewee](https://docs.peewee-orm.com/) methods

|     |     |
| --- | --- |
| Model.create_table() |  |
| Model.save() | calls `deta.Base(tabel_name).put( dirty_fields or all columns )` |
| Model.insert() | calls .save() |
| Model.create() | calls .save() |
| Model.update() | not wrapped |
| Model.Meta.deta | `deta.Deta(DETA_KEY)` |
| Model.Meta.mirrored | always sync full table, after create & before exit , `False` default |

## how it work
<!--
no complete match
approximate mirroring
has limited compatibility

create
insert
update
save

load
dump
-->

## License
* It's opensource and free software, see the [LICENSE](LICENSE) for more details

## similar projects
* [ssqlite3](https://github.com/jnsougata/space-sqlite3/) store binary `datafile.sqlite3` in DetaBase tables
* [ODetaM](https://github.com/rickh94/ODetaM/) Object Document Mapper for DetaBase based on pydantic
* [detadantic](https://github.com/Jay184/detadantic/) Active-Record style wrappers to Deta Base
* [deta-base-pydantic](https://github.com/papalotis/deta-base-pydantic/) 
* [csv-deta](https://pypi.org/project/csv-deta/)  

## TODO
