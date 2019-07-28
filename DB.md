### Employee(雇员)
* Long id
* String name @NotNull
* String email @Unique @NotNull
* String phone @Unique @NotNull
* String password @Encrypt
* Integer status default '下班' `['下班', '上班', '迟到', '请假']`
* Integer 职位 default '泊车仔'   

### Order
* Long id
* String CarNo @NotNull
* Long parkingLotId 
* Long employeeId
* Integer type @NotNull
* Long createAt @NotNull (创建时间)
* Long appointTime @NotNull
* Integer status default '无人处理' `['派单中', '无人处理', '已完成']`

### Parking lot
* Long id
* Long 雇员id
* String name @Unique @NotNull
* Integer size @NotNull (>= 0)
* Boolean isActive default true
* Integer parkedNum default 0 

###  Office
* Integer id
* String title @NotNull @Unique
