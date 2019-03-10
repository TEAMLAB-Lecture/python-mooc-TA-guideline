# theteamlab.io 신규 학생 등록 메뉴얼

## 

````python
with open('dd.csv', 'r') as csvfile:
  student = csv.reader(csvfile, delimiter=',', quotechar='|')
  studnet_list = []
  for row in student:
    t = TeamlabUser(username=row[0])
    t.set_password(row[1])
    t.save()
```
