# [naming-conventions](https://github.com/mickey-ichi/js-training/blob/master/naming-conventions.md)

## Table of Contents

1. [Naming Function / Variable](#naming-function--variable)
1. [Naming Constant](#naming-constant)
1. [Naming Component](#naming-component)
1. [Notes for naming](#notes-for-naming)
1. [Naming convention for boolean value](#naming-convention-for-boolean-value)
1. [Naming convention for action related to string value](#naming-convention-for-action-related-to-string-value)
1. [Naming convention for data manipulation (Add)](#naming-convention-for-data-manipulation-add)
1. [Naming convention for data manipulation (Update)](#naming-convention-for-data-manipulation-update)
1. [Naming convention for data manipulation (Delete)](#naming-convention-for-data-manipulation-delete)
1. [Naming convention for data manipulation (Write)](#naming-convention-for-data-manipulation-write)
1. [Naming convention for data manipulation (Read)](#naming-convention-for-data-manipulation-read)
1. [Naming convention for data manipulation (Verification/Check/Validation)](#naming-convention-for-data-manipulation-verificationcheckvalidation)
1. [Naming convention for permission / prohibition](#naming-convention-for-permission--prohibition)


## Naming Function / Variable

Camelcase (Lower camel case): chữ cái đầu tiên của từ ghép là chữ thường

```javascript
// bad
const OBJEcttsssss = {};
const this_is_my_object = {};
function c() {}

// good
const thisIsMyObject = {};
function thisIsMyFunction() {}
```

```typescript
// bad
const OBJEcttsssss: Object = {};
const this_is_my_object: any = {};
function c() {}

// good
const thisIsMyObject: User = {};
function thisIsMyFunction(params: Params): void {}
```


## Naming Constant

Snake Case (All Caps): viết hoa tất cả các chữ cái và nối từ bằng dấu \_\

```javascript
// bad
const OBJEcttsssss = {};
const this_is_my_object = {};

// good
const GUEST_ROLE = 'guest';
const PREMIUM_ROLE = 'premium';
const API_URL = 'api_url';
```

```typescript
// bad
const OBJEcttsssss = {};
const this_is_my_object = {};

// good
const GUEST_ROLE: string = 'guest';
const PREMIUM_ROLE: string = 'premium';
const API_URL: string = 'api_url';
```


## Naming Component

Pascal case (Upper camel case): chữ cái đầu tiên của từ ghép là chữ Hoa

```javascript
// bad
function c() {}
class c extend React.Component {}

// good
function Component() {}
class Component extend React.Component {}
const Component = () => {}
```

```typescript
// bad
function c() {}
class c extend React.Component {}

// good
function Component(props: Props) {}
class Component extend React.Component<Props, State> {}
const Component: FC<Props> = (props) => {}
```

## Notes for naming

Gợi ý:
- variable name, class name, component name, file name luôn luôn là danh từ.
- function name luôn luôn là động từ.

Dùng từ rõ ràng: Khi dùng những từ trừu tượng, hãy bao gồm thông tin rõ ràng như "ở đâu" và "cái gì" trong cách đặt tên.

Tránh những tên chung chung:
- Khi đặt tên, hãy cân nhắc xem chúng có mục đích gì
- Các biến để lưu trữ tạm thời thì là ngoại lệ


Tránh những tên dài: Thiết kế tên sao cho dài nhất có khoảng 20 ký tự. Tên dài khó đọc hơn, gõ rườm rà và gây ra lỗi chính tả. Ngoài ra, nếu từ viết tắt phổ biến như một quy ước, hãy làm theo ví dụ sau:(Ex：`average` thì viết thành `avg`

Đặt tên sao cho  dễ hiểu: Nếu tên viết tắt và nhầm lẫn với các yếu tố khác, hãy sử dụng tên có thể hiểu được mà không cần viết tắt nhiều hơn mức cần thiết.

Sử dụng một tên cụ thể: Bao gồm cụ thể những thông tin mà biến hoặc hàm đó đảm nhiệm .

Xác định từ trái nghĩa: Xác định đúng các từ trái nghĩa để có sự thống nhất trong quy ước đặt tên.
-   `Start` ⇔ `Stop`
-   `Top` ⇔ `Bottom`
-   `High` ⇔ `Low`
-   `Big` ⇔ `Small`
-   `Attach` ⇔ `Detach`
-   `Input` ⇔ `Output`
-   `Show` ⇔ `Hide`


Thêm thông tin bằng cách sử dụng hậu tố / Prefix: Đặt một đơn vị vào biến lưu trữ giá trị.(`px` hoặc `ms` )


## Naming convention for boolean value

Naming convention for boolean value

| Place | Word | Meaning| Example|
|---|---|---|---|
| Prefix	 | is | Đang ở trong trạng thái gì không ?	 | isEnabled |
| Prefix	 | can | Có thể xử lí được không?	 | canRemove |
| Prefix	 | should | Có nên thực hiện lệnh không?| shouldMigrate |
| Prefix	 | need | Có cần thực hiện gì không?| needFileCopy |
| Prefix	 | has | Có cái data/ properties mong muốn không| hasConnection |
| Prefix	 | exists | Có tồn tại data hoặc properties mong muốn không?| exists(dir) |
| Prefix	 | contains | Có chứa data hay properties không?| contains(item) |


## Naming convention for action related to string value

Naming convention for action related to
string value

| Place | Word | Meaning| Example|
|---|---|---|---|
| Prefix	 | find | Tìm thông tin(tiền đề cho việc có thể tìm thấy)| findString |
| Prefix	 | search | Tìm thông tin(tiền đề cho việc không thể tìm thấy)| searchString |
| Prefix	 | seek | Tìm thông tin liên tục theo thứ tự| file.seek() |
| Prefix	 | extract | Extract thông tin theo điều kiện| hash.extract() |
| Prefix	 | filter | Loại trừ thông tin theo các điều kiện nhất định| filter() |
| Prefix	 | replace | Thay thế dữ liệu hiện có| String.replace() |
| Prefix	 | join | Kết hợp dữ liệu hiện có| String.join() |
| Prefix	 | parse | Phân tích dữ liệu hiện có| String.Parse() |


## Naming convention for data manipulation (Add)

Naming convention for data manipulation (add)

| Place | Word | Meaning| Example|
|---|---|---|---|
| Prefix	 | set | Set data | setProperty |
| Prefix	 | add | Thêm data hoặc object| addList |
| Prefix	 | put | Thêm data hoặc object| hash.put(key,value) |
| Prefix	 | insert | Chèn data hoặc object| insertQueue |
| Prefix	 | append | Thêm data hoặc object vào cuối| appendQueue |
| Prefix	 | push | Thêm data hoặc object vào vị trí đầu| pushQueue |
| Prefix	 | prepend | Thêm data hoặc object vào vị trí đầu| prependQueue |
| Prefix	 | register | Đăng kí data hoặc object| registerStorage |
| Prefix	 | create | Tạo data hoặc file mới| createAccount |
| Prefix	 | new | Tạo data hoặc file mới| newAccount |
| Prefix	 | make | Xử lí data cũ để tạo data hoặc file mới| makeFile |
| Prefix	 | build | Tập hợp dữ liệu và tệp từ dữ liệu hiện có| buildFile |
| Prefix	 | from | Sử dụng data hiện có để tạo file hoặc data| fromConfigFile |
| Prefix	 | generate | Tạo file hoặc data theo 1 rule nào đó| generateFile |


## Naming convention for data manipulation (Update)

Naming convention for data manipulation(update)

| Place | Word | Meaning| Example|
|---|---|---|---|
| Prefix	 | update | Update data cũ| updateAccount |
| Prefix	 | upgrade | Thay đổi data thành cái tốt hơn| upgradeAccount |
| Prefix	 | apply | Áp dụng data có sẵn| applyAccount|
| Prefix	 | refresh | Cập nhật lại data cũ| refreshAccount |
| Prefix	 | changed | Thay đổi data hiện có| changedAccount |
| Prefix	 | modified | Sửa data có sẵn| modifiedAccount |
| Prefix	 | revised | Sửa data có sẵn| revisedAccount |
| Prefix	 | enable | Enable khả năng sử dụng của data có sẵn| enableAccount |
| Prefix	 | disable | Disable khả năng sử dụng của data có sẵn| disableAccount |
| Prefix	 | fix | Giải quyết vấn đề của data| fixAccount |
| Prefix	 | repair | Sửa data| repairAccount |
| Prefix	 | restore | Restore data| restoreAccount |
| Prefix	 | recover | Recover data| recoverAccount |
| Prefix	 | edit | Edit data| editAccount |
| Prefix	 | adjust | Điều chỉnh data| adjustString |
| Prefix	 | adapt | Điều chỉnh dữ liệu hiện có| adaptString |
| Prefix	 | convert | Chuyển đổi dữ liệu hiện có| convertString |
| Prefix	 | to | Chuyển đổi dữ liệu hiện có sang cái gì| toString |


## Naming convention for data manipulation (Delete)

Naming convention for data manipulation(delete)

| Place | Word | Meaning| Example|
|---|---|---|---|
| Prefix	 | delete | Xoá data hiện có( không revert được)|deleteAccount
| Prefix	 | remove | Xoá data hiện có(revert được)| removeAccount |
| Prefix	 | trash | Xoá data hiện có(có revert được)| trashAccount|
| Prefix	 | erase | Xóa dữ liệu hiện có (có thể ghi lại)| eraseAccount |
| Prefix	 | clear | Clear data hiện có về trạng thái khởi tạo| clearAccount |
| Prefix	 | flush | Xoá data về trạng thái ban đầu| flushAccount |
| Prefix	 | reset | Reset data về trạng thái ban đầu| resetAccount |
| Prefix	 | dispose | Giải phóng dữ liệu hiện có(có thể tái sử dụng)| disposeAccount |
| Prefix	 | destroy | Loại bỏ dữ liệu hiện có (không thể sử dụng lại)| destroyAccount |
| Prefix	 | unregister | Hủy dữ liệu đã đăng ký| unregisterStorage |
| Prefix	 | unset | Bỏ định nghĩa data đã được định nghĩa| unsetAccount |
| Prefix	 | pop | Trích xuất và loại bỏ dữ liệu đầu tiên| popQueue |
| Prefix	 | initialize | Khởi tạo dữ liệu hiện có| initialize() |
| Prefix	 | edit | Edit data| editAccount |
| Prefix	 | adjust | Điều chỉnh data| adjustString |
| Prefix	 | adapt | Điều chỉnh dữ liệu hiện có| adaptString |
| Prefix	 | convert | Chuyển đổi dữ liệu hiện có| convertString |
| Prefix	 | to | Chuyển đổi dữ liệu hiện có sang cái gì| toString |


## Naming convention for data manipulation (Write)

Naming convention for data manipulation(write)

| Place | Word | Meaning| Example|
|---|---|---|---|
| Prefix	 | save | Lưu data hiện có|saveAccount
| Prefix	 | output | Xuất dữ liệu hiện có| outputAccount |
| Prefix	 | export | Xuất dữ liệu hiện có| exportAccount|
| Prefix	 | write | Write dữ liệu hiện có| writeAccount |
| Prefix	 | store | Store dữ liệu hiện có| storeAccount |
| Prefix	 | send | Gửi data hiện có| sendAccount |
| Prefix	 | commit | Xác định data| commitAccount |


## Naming Convention for data manipulation (Read)

Naming Convention for data manipulation (Read)

| Place | Word | Meaning| Example|
|---|---|---|---|
| Prefix	 | get | Get data hiện có|getAccount
| Prefix	 | load |Load data hiện có| loadAccount |
| Prefix	 | input | Nhập data hiện có| inputAccount|
| Prefix	 | import | Import data hiện có| importAccount |
| Prefix	 | read | Read data| readAccount |
| Prefix	 | restore | Restore data hiện có| restoreAccount |
| Prefix	 | fetch | Get data hiện có| fetchAccount |


## Naming convention for data manipulation (Verification/Check/Validation)

Naming convention for data manipulation(verification)

| Place | Word | Meaning| Example|
|---|---|---|---|
| Prefix	 | check | Check data có phù hợp với điều kiện không|checkAccount
| Prefix	 | test |Check xem data có thoả mãn điều kiện không| testAccount |
| Prefix	 | validate | Validate data có đúng không| validateAccount|
| Prefix	 | compare |So sánh data| compareAccount |
| Prefix	 | verify | Verify data| verifyAccount |


## Naming convention for permission / prohibition

Naming convention for permission / prohibition

| Place | Word | Meaning| Example|
|---|---|---|---|
| Prefix	 | allow | Cấp quyền sử dụng|allowAccount
| Prefix	 | disallow |Bỏ cấp quyền sử dụng| disallowAccount |
| Prefix	 | accept | Chấp nhận| acceptAccount|
| Prefix	 | deny |Deny| denyAccount |
| Prefix	 | refuse | Từ chối yêu cầu| refuseAccount |
| Prefix	 | reject | Từ chối  yêu cầu| rejectAccount |
| Prefix	 | grant | Cung cấp một loạt các quyền| grantAccount |
| Prefix	 | revoke | Tước quyền| revokeAccount |
