# GORM PostgreSQL Driver

## Quick Start

```go
import (
  "github.com/yugabyte/gorm-yugabytedb"
  "gorm.io/gorm"
)

// https://github.com/yugabyte/pgx
baseUrl := fmt.Sprintf("postgres://%s:%s@%s:%d/%s",
		user, password, host, port, dbname)
	url := fmt.Sprintf("%s?load_balance=true&yb_servers_refresh_interval=240", baseUrl)
db, err := gorm.Open(postgres.Open(url), &gorm.Config{})
```

## Configuration

```go
import (
  "github.com/yugabyte/gorm-yugabytedb"
  "gorm.io/gorm"
)

	baseUrl := fmt.Sprintf("postgres://%s:%s@%s:%d/%s",
		user, password, host, port, dbname)
	url := fmt.Sprintf("%s?load_balance=true&yb_servers_refresh_interval=240", baseUrl)

db, err := gorm.Open(postgres.Open(url), &gorm.Config{
		Logger: logger.Default.LogMode(logger.Info),
	})
	if err != nil {
		panic(err)
	}
```
