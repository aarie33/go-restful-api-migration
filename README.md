# GO DATABASE MIGRATION
- Golang Migrate
- go install -tags 'postgres,mysql' github.com/golang-migrate/migrate/v4/cmd/migrate@latest

## Migrate
- `migrate create -ext sql -dir db_migrations create_table_category` would create up and down sql file
- `migrate -database "mysql://root@tcp(localhost:3306)/test-go" -path db_migrations up` would run all migration
- rollback with number of migration `migrate -database "mysql://root@tcp(localhost:3306)/test-go" -path db_migrations down 1`
- change version when meet dirty state `migrate -database "mysql://root@tcp(localhost:3306)/test-go" -path db_migrations force VERSION`
- check version `migrate -database "mysql://root@tcp(localhost:3306)/test-go" -path db_migrations version`

## Slide Go lang DB
<a href="https://docs.google.com/presentation/d/1GDOmXHIoxKfm2k2ku9gD1u-VpsEri6G-MJEMMTufDug/edit?usp=sharing" target="_blank">Here</a>

## Code Ref
<a href="https://github.com/ProgrammerZamanNow/belajar-golang-database-migration" target="_blank">Here</a>
