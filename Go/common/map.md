 
```go
type Person struct {
     Name []string
     Age int
 }
 
temp := map[string]Person{
  "citizen":{
    Name: []string{"John","Dongju"},
    Age:20,
  },
}

temp["citizen"].Name= append(temp["citizen"].Name, "david")
```
<p>cannot assign to struct field temp["citizen"].Name in map</p>
<ul>
  <li>golang에서 map(hash map)의 경우 사이즈가 커질수록 buctket을 증가시키면서 해당 값을 복제한다. </li>
  <li>즉, dynamic하게 구성되는 데이터 구조임으로, 키-값 쌍이 고정되어 있지 않기 때문에 addressable한 값으로 지정되어 있습니다</li>
</ul>
