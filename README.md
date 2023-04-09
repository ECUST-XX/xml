增加了支持短标签(自关闭标签)功能的golang xml官方包.

Added official package of golang xml with shortform (auto close) support.

# How to get
```
go get github.com/ECUST-XX/xml
```
# Usage

Replace

```go
import "encoding/xml"
xml.MarshalIndent(v, "  ", "    ")
```

with

```go
import "github.com/ECUST-XX/xml"
xml.MarshalIndentShortForm(v, "  ", "    ")
```

or

```go
import "github.com/ECUST-XX/xml"
enc := xml.NewEncoder(os.Stdout)
enc.Indent("  ", "    ")
enc.ShortForm()
if err := enc.Encode(v); err != nil {
    fmt.Printf("error: %v\n", err)
}
```