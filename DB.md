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
* Long employeeId
* Long userId @NotNull
* Long parkingLotId 
* String carNumber @NotNull
* Long endAt (结束时间)
* Long createAt @NotNull (创建时间)
* Long appointTime @NotNull (预约时间)
* String appointAddress @NotNull (预约交车地点)
* Integer status default '无人处理' `['无人处理', '停车中', '已停车', '取车中', '已完成']`
> 无人处理: 用户下单, 还没小哥抢单
> 停车中:   小哥抢单后
> 已停车:   小哥点击已停车按钮
> 取车中:   用户点取车按钮
> 已完成:   小哥点击已取车按钮

### User
* Long id
* String password @Encrypt
* String phone @Unique @NotNull

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
