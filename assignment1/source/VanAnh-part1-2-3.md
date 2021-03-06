#Thiết kế phần mềm#
##Giới thiệu##
Khái niệm thiết kế được định nghĩa theo 2 cách sau:
  -  **Thiết kế** là quy trình định nghĩa ra kiến trúc, thành phần, interfaces và các thuộc tính khác của một hệ thống hoặc một thành phần. 
  Trong quy trình này, yêu cầu phần mềm được phân tích để đưa ra một cấu trúc của phần mềm làm cơ sở để làm ra phần mềm. 
  -  **Thiết kế** là kết quả của một quá trình. Nó mô tả kiến trúc của một phần mềm như là phần mềm được phân rã và tổ chức như thế nào trong các thành phần và các interfaces giữa các thành phần như thế nào. Nó cũng có thể mô tả các thành phần ở mức chi tiết cho phép có thể xây dựng được phần mềm.

**Thiết kế phần mềm** đóng vai trò quan trọng: trong suốt quá trình thiết kế, những kỹ sư phần mềm sẽ đề xuất các mô hình tạo thành loại kế hoạch chi tiết cho giải pháp để có thể thực hiện được. Chúng ta có thể phân tính và đánh giá những mô hình này có hay không phù hợp với những yêu cầu khác nhau. Chúng ta có thể sử dụng kiểm tra và thẩm định thay thế những giải pháp và những đánh đổi (tradeoffs). Cuối cùng chúng ta sử dụng những mô hình kết quả để lên kế hoạch các hoạt động phát triển tiếp theo như là: thẩm định và kiểm thử hệ thống, thêm vào đó sử dụng chúng như là đầu vào hay là điểm bắt đầu của xây dựng và kiểm thử phần mềm.

Trong danh sách chuẩn của vòng đời phát triển phần mềm như ISO/IEC/IEEE Software Life Cycle Process, thiết kế phần mềm bao gồm 2 hoạt động tương ứng với phân tích yêu cầu phần mềm và xây dựng phần mềm:

- **Thiết kế kiến trúc** (còn được gọi là thiết kế mức cao): là phát triển mức kiến trúc cao nhất và đưa ra cách tổ chức phần mềm và chỉ ra các thành phần khác nhau trong phần mềm

- **Thiết kế chi tiết**: chỉ ra chi tiết và đầy đủ về thành phần tạo điều kiện xây dựng phần mềm trong pha sau đó

Đầu ra của thiết kế phần mềm sẽ được sử dụng cho quá trình xây dựng và kiểm thử nên việc đánh giá một thiết kế có phù hợp hay không rất quan trọng, nếu một thiết kế sai sẽ dẫn đến tất cả các quá trình sau đó cũng sai và cần phải chỉnh sửa nếu thiết kế được chỉnh sửa.

##1. Nguyên tắc thiết kế phần mềm cơ bản##

Phần này đưa ra khái niệm, quan niệm và thuật ngữ hình thành nền tảng cơ bản để hiểu biết về vai trò và phạm vi của thiết kế phần mềm

###1.1	Khái niệm thiết kế chung ###

Theo nghĩa chung, thiết kế có thể được xem như là một hình thức giải quyết vấn đề.

###1.2	Bối cảnh của thiết kế phần mềm###

Thiết kế phần mềm là một phần quan trọng của quy trình phát triển phần mềm. Để hiểu vai trò của thiết kế phần mềm, chúng ta có thể nhìn và vòng đời phát triển phần mềm để thấy nó là một thành phần gắn với vòng đời này.

###1.3	Quy trình thiết kế phần mềm###

Thiết kế phần thường được xem như là một quy trình 2 bước:

- Thiết kế kiến trúc (cũng được xem như là thiết kế mức cao high- level design or top- level design) mô tả phầm mềm được tổ chức thành các thành phần như thế nào

- Thiết kế chi tiết mô tả hành động mong muốn của những thành phần

Đầu ra của 2 quy trình này là tập mô hình và tài liệu ghi lại những những quyết định quan trọng đã được thực hiện cùng lời giải thích cho mỗi lý do. Bằng cách ghi lại các lý do đó công việc bảo trì dài hạn của phần mềm được nâng cao

###1.4	Nguyên tắc thiết kế phần mềm###

**Nguyên tắc** là “một giả định, giáo lý hoặc luật căn bản và toàn diện”. **Nguyên tắc thiết kế phần mềm** là quan niệm chính cung cấp kiến thức cơ bản cho khái niệm và hướng tiếp cận thiết kế phần mềm khác nhau. Nguyên tắc thiết kế phần mềm bao gồm: trừu tượng hóa (abstraction); ghép nối và liên kết (coupling and conhesion); phân rã và modul hóa (decomposition and modularization); đóng gói/ẩn thông tin (encapsulation/information hiding); tách giao diện và thực hiện (separation of interface and implementation); đầy đủ, toàn vẹn và nguyên thủy (sufficiency, completeness, and primitiveness); và tách mối quan tâm (separation of cencerns)

- **Abstraction**: là một cách nhìn của một đối tượng mà tập trung vào thông tin liên quan để cụ thể hóa mục đích và tránh bỏ xót thông tin”. Trong bối cảnh của thiết kế phần mềm, 2 cơ chế trừu tượng hóa chìa khóa là tham số hóa và cụ thể hóa. Trừu tượng bởi tham số hóa trừu tượng đến từ biểu diễn dữ liệu chi tiết bởi biểu diễn dữ liệu như tên những tham số. Trừu tượng hóa bởi cụ thể hóa dẫn đến 3 loại trừu tượng: trừu tượng thủ tục, trừu tượng dữ liệu và trừu tượng điều khiển (trừu tượng tương tác lẫn nhau)
 - Trừu tượng thủ tục (trừu tượng hàm) cung cấp cơ chế để trừu tượng những thủ tục dễ định nghĩa hoặc những thao tác thành những thực thể. Trưu tượng thủ tục đã được áp dụng rộng rãi và các ngôn ngữ lập trình hầu như tất cả đều cung cấp hỗ trợ khái niệm này (ví dụ pascal, java,...)
 - Trừu tượng dữ liệu: đây là nguyên tắc chính trong hướng đối tượng. Trong kiểu trừu tượng này, thay vì chỉ tập trung vào thao tác, chúng ta tập trung và dữ liệu đầu tiên và sau đó những thao tác tác động lên dữ liệu. Một ví dụ đơn giản là queue data và những thao tác liên quan như add() and delete(). Trong trừu tượng hóa thủ tục, thao tác add và delete chỉ là riêng biệt không có quan hệ với dữ liệu. Điểm mạnh của trừu tượng hóa dữ liệu so với trừu tượng hóa thủ tục là dữ liệu và các thao tác liên quan được đưa ra vì vậy rất dễ để sửa code khi dữ liệu thay đổi.
 - Trừu tượng điều khiển liên quan để sử dụng các chương trình con và liên quan đến luồng điều khiển.

- **Coupling and Conhesion**: Ghép nối là một độ đo của độ phụ thuộc lẫn nhau giữa các module trong chương trình máy tính, trong khi đó liên kết là độ đo độ mạnh của mối liên kết giữa các phần tử trong một module.

- **Phân rã hóa và module hóa**: Phân rã hóa và modul hóa nghĩa là phần mềm lớn được chia thành một số thành phần định danh (dễ định nghĩa interface) mà mô tả tương tác giữa các thành phần. Thông thường mục tiêu là thay thế những chức năng và trách nhiệm trong những thành phần khác nhau.

- **Đóng gói và ẩn thông tin**: nghĩa là nhóm và đóng gói chi tiết bên trong của một trừu tượng và làm cho những chi tiết không thể được truy cập từ bên ngoài

- **Tách giao diện và thực hiện** liên quan đến việc xác định mọt thành phần bằng cách xác định một giao diện public (được biết đến như là client) mà là tách từ chi tiết của thành phần được hiện thực hóa như thế nào.

- **Tính đầy đủ, toàn vẹn và nguyên thủy**: mục tiêu của tính đầy đủ, toàn vẹn và nguyên thủy nghĩa là chắc rằng một thành phần chỉ tương ứng với những đặc điểm quan trọng của một trừu tượng. Nguyên thủy nghĩa là thiết kế nên được dựa trên mô hình dễ thực hiện

- **Tách mối quan tâm**. Một mối quan tâm là một “khu vực quan tâm với sự liên quan đến thiết kế phần mềm”. Một mối quan tâm thiết kế là một lĩnh vực của thiết kế mà liên quan đến một hay nhiều các bên liên quan (stakeholders). Mỗi kiến trúc nhìn một hay nhiều khung nhìn quan tâm. Tách mối quan tâm bởi những khung nhìn cho phép quan tâm các bên liên quan (stakeholders) tập trung vào một việc tại một thời điểm và yêu cầu và cung cấp một phương tiện quản lý phức tạp.

##2.	Những vấn đề chính trong thiết kế kiến trúc phần mềm##

Một số vấn đề quan trọng phải được xử lý trong khi thiết kế phần mềm. Đặc biệt là những lo ngại về chất lượng phần mềm mà có thể kể đến như: hiệu suất, bảo mật, độ tin cậy, khả năng sử dụng, vv... Một số vấn đề quan trọng khác là làm thế nào để phân rã, tổ chức và đóng gói những thành phần phần mềm. Đây là nguyên tắc cơ bản mà tất các các phương pháp thiết phải giải quyết nó bằng cách này hay cách khác. Ngược lại, những vấn đề “liên quan đến các khía cạnh của các hành vi phần mềm mà lại không nằm trong miền ứng dụng mà nằm ở các miền khác có liên quan” Những vấn đề đó thường xuyên chồng chéo với các chức năng của hệ thống và được gọi những khía cạnh mà đa phần không phải là đơn vị phân rã của phần mềm mà là thuộc tính ảnh hưởng đến hiệu suất hoặc ngữ nghĩa của các thành phần một cách có hệ thống.

###2.1	Đồng thời (concurrency)###

Đồng thời là nhiều việc xảy ra tại cùng một thời điểm. Thiết kế để có tính đồng thời có liên quan đến phân rã phần mềm thành quy trình, nhiệm vụ, quá trình và đối phó với các vấn đề liên quan đến tính hiệu quả, tính nguyên tố, đồng bộ hóa và lập kế hoạch. Thiết kế này đảm bảo dễ phân chia công việc cũng như có thể hoàn thành công việc trong thời gian ngắn nhất.

###2.2	Điều khiển và xử lý các sự kiện###

Vấn đề thiết kế này liên quán tới làm thế nào tổ chức dữ liệu và dòng dữ liệu cũng như làm thế nào để xử lý các sự kiện tạm thời và phản xạ qua các cơ chế lời gọi ngầm và gọi lại.

###2.3	Dữ liệu bền vững (data persistence)###

Vấn đề của thiết kế này liên quan tới làm thế nào để xử lý dữ liệu tồn tại lâu dài

###2.4	Phân phối các thành phần###

Vấn đề của thiết kế này liên quan đến làm thế nào để phân phối các phần mềm trên phần cứng ( bao gồm phần cứng máy tính và phần cứng mạng), làm thế nào các thành phần giao tiếp được với nhau, và làm thế nào tầng giữa có thể được sử dụng để đối phó với không tương thích phần mềm.

##2.5	Lỗi và xử lý ngoại lệ và lỗi dung nạp (error and exception handling and fault tolerance)##

Vấn đề của thiết kế này liên quan đến làm thế nào để phòng chống, chịu đựng và các xử lý lỗi và đối phó với các điều kiện ngoại lệ

###2.6	Tương tác và trình bày (Interaction and presentation)###

Vấn đề thiết kế này liên quan tới làm thế nào để cấu trúc và tổ chức tương tác với những người dùng và biểu diễn thông tin ( ví dụ, chia giao diện và khung nhìn logic sử dụng hướng tiếp cận MVC)

Chú ý rằng chủ đề này không chỉ chi tiết giao diện người dùng, đó là nhiệm vụ của thiết kế giao diện người dùng

###2.7	Bảo mật (sercurity)###

Thiết kế cho bảo mật liên quan đến làm thế nào để ngăn chặn tiết lộ trái phép, sáng tạo, thay đổi, xóa, hoặc từ chối truy cập đến thông tin từ các nguồn khác. Nó cũng quan tâm làm thế nào để chịu được các cuộc tấn công bảo mật hoặc sự xâm phạm bởi hạn chế thiệt hại, tiếp tục dịch vụ, tốc độ sửa chữa và phục hồi, và thất bại và phục hồi an toàn. Kiểm soát truy cập là một khái niệm an ninh cơ bản và ta cũng nên đảm bảo sử dụng đúng mật mã

##3.	Kiến trúc và cấu trúc phần mềm##

**Một kiến trúc phần mềm** là “tập hợp các cấu trúc cần thiết để suy luận về hệ thống, trong đó bao gồm các yếu tố phần mềm, mối quan hệ giữa chúng và đặc tính của cả hai. Trong suốt những năm 1990, kiến trúc phần mềm bắt đầu nổi lên như một ngành học rộng liên quan đến việc nghiên cứu các cấu trúc phần mềm và kiến trúc theo một cách chung. Điều đó dẫn đến một số khái niệm thú vị về thiết kế phần mềm ở những mức độ khác nhau của trừu tượng hóa. Mội số khái niệm có thể hữu ích trong việc thiết kế kiến trúc ( ví dụ phong cách kiến trúc) cũng như trong suốt quá trình thiết kế chi tiết (ví dụ design pattern). Những khái niệm thiết kế này cũng được sử dụng để thiết kế những chương trình tương tự.

###3.1	Cấu trúc và góc nhìn###

Khía cạnh mức cao khác nhau của thiết kế phần mềm có thể được mô tả và tài liệu hóa. Những khía cạnh này thường được gọi là các góc nhìn “Một góc nhìn biểu diễn một phần khía cạch của kiến trúc phần mềm mà biểu diễn cụ thể chính xác của hệ thống phần mềm”. Các góc nhìn thích hợp với những vấn đề khác nhau liên quan đến phần mềm – ví dụ, góc nhìn logic (đáp ứng các yêu cầu chức năng) với góc nhìn tiến trình (vấn đề đồng thời) với góc nhìn vật lý (vấn đề phân phối) với góc nhìn phát triển (làm thế nào để thiết kế được break down thành các thành phần đơn vị với đại diện rõ ràng của sự phụ thuộc giữa các đơn vị). Nhiều tác giả sử dụng những thuật ngữ khác nhau- như hành vi, chức năng, cấu trúc, góc nhìn mô hình dữ liệu. Tóm lại, thiết kế phần mềm là nhiều khía cạnh sản xuất bởi quá trình thiết kế và cấu tạo từ quan điểm độc lập tương đối và những góc nhìn trực giao.

###3.2	Kiểu kiến trúc###

**Kiểu kiến trúc** là một chuyên môn hóa của phần tử và các loại liên quan, cùng với một bộ những hạn chế về cách nó có thể được sử dụng. Môt vài tác giải chỉ ra một số kiểu kiến trúc chính như sau:

- Kiến trúc thường (ví dụ, phân tâng, pipes and filter, blackboard)

- Các hệ thống phân tán (ví dụ client- server, three- tiers, broker)

- Các hệ thống tương tác (ví dụ, MVC, Presentation- Abstraction- Control, WPF)

- Các hệ thống mô phỏng (ví dụ, microkernel, reflection)

- Các kiểu khác (ví dụ, batch, interperters, process control, rule- based)

###3.3	Mẫu thiết kế (Design Patterns)###

Mẫu là một giải pháp phổ biến để giải quyết các vấn đề phồ biến trong ngữ cảnh đưa ra. Trong khi kiểu kiến trúc có thể được nhìn như mẫu mô tả tổ chức mức cao của phần mềm, mẫu thiết kế có thể sử dụng mô tả cụ thể ở mức thấp. Những mẫu thiết kế mức thấp bao gồm:

- Mẫu tạo (ví dụ, builder, factory, prototype, singleton)

- Mẫu cấu trúc (ví dụ, adapter, bridge, composite, decorator, façade, fly- weight, proxy)

- Mẫu hành vi (ví dụ, command, interperter, iterator, mediator, memento, observer, state, strategy, template, visitor)

###3.4	Những quyết định thiết kế kiến trúc###
Thiết kế kiến trúc là một quá trình sáng tạo. Trong suốt quy trình thiết kế, nhà thiết kế phần mềm phải tạo một số quyết định cơ bản ảnh hưởng sâu sắc tới các phần mềm và quy trình phát triển phần mềm. Nên nghĩ rằng thiết kế kiến trúc tạo thành từ quan điểm quyết định hơn là quan điểm hoạt động. Thông thường, tác động vào chất lượng thuộc tính và hoán đổi giữa các thuộc tính cạnh trạnh là cơ sở cho quyết định thiết kế

###3.5	Tương tự giữa chương trình và framework###

Một cách tiếp cận cung cấp cho việc sử dụng lại thiết kế phần mềm và thành phần là sử dụng những chương trình tương tự. Điều này có thể thực hiện bằng xác định sự tương đồng giữa các phần mềm bằng cách thiết kế các thành phần tái sử dụng và tùy vào sự khác nhau giữa các phần mềm. Trong lập trình hướng đối tượng, một khái niệm chìa khóa có liên quan đến khung là một khung: một phần hệ thống phần mềm hoàn toàn có thể được mở rộng bằng cách cài đặt các công cụ thích hợp

