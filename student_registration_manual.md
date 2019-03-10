# theteamlab.io 신규 학생 등록 메뉴얼

## 

Google sheets에서 암호를 임의로 생성하는 방법
```bash
=CHOOSE(RANDBETWEEN(1,2),CHAR(RANDBETWEEN(48,57)),
                         CHAR(RANDBETWEEN(65,90)))&
 CHOOSE(RANDBETWEEN(1,2),CHAR(RANDBETWEEN(48,57)),
                         CHAR(RANDBETWEEN(65,90)))&
 CHOOSE(RANDBETWEEN(1,2),CHAR(RANDBETWEEN(48,57)),
                         CHAR(RANDBETWEEN(65,90)))&
 CHOOSE(RANDBETWEEN(1,2),CHAR(RANDBETWEEN(48,57)),
                         CHAR(RANDBETWEEN(65,90)))&
 CHOOSE(RANDBETWEEN(1,2),CHAR(RANDBETWEEN(48,57)),
                         CHAR(RANDBETWEEN(65,90)))&
 CHOOSE(RANDBETWEEN(1,2),CHAR(RANDBETWEEN(48,57)),
                         CHAR(RANDBETWEEN(65,90)))&
 CHOOSE(RANDBETWEEN(1,2),CHAR(RANDBETWEEN(48,57)),
                         CHAR(RANDBETWEEN(65,90)))&
 CHOOSE(RANDBETWEEN(1,2),CHAR(RANDBETWEEN(48,57)),
                         CHAR(RANDBETWEEN(65,90)))
```
```python
import csv
from account.models import TeamlabUser

with open('dd.csv', 'r') as csvfile:
  student = csv.reader(csvfile, delimiter=',', quotechar='|')
  studnet_list = []
  for row in student:
    t = TeamlabUser(username=row[0])
    t.set_password(row[1])
    t.save()
```
