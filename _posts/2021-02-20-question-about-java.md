---
layout: post
title: Vài điều thắc mắc về Java
image: /img/avatar-java.png
tags: [java]
---

<ol>
  <li><a href="#1-some-key-word">SDK, JDK, JRE, Java SE, Java EE, Java ME, JVM, JIT bla bla :scream:</a></li>
  <li><a href="#2-java-version">Java version</a></li>
</ol>


<div id="1-some-key-word"></div>

### 1. Một vài thuật ngữ: JDK, JRE...

Trước hết hãy đọc <a href="https://www.facebook.com/namdotnet/posts/1400347743483571" target="_blank">bài viết Giới thiệu về Java trên page Nam .NET.</a>  
Tóm tắt:
<ul>
  <li>Cái tên Java => chỉ 3 phần khác nhau: ngôn ngữ Java, Java Runtime, các thư viện Java => gom lại: Java Platform.</li>
  <li>Java runtime là tất cả những gì cần để chương trình Java thực thi</li>
  <li>Các tập thư viện Java chia làm 3 loại chính, theo các lớp thiết bị khác nhau:</li>
  <ul>
    <li>Java SE - Java Standard Edition: bộ Java cơ bản, chứa các thành phần chính để chương trình Java chạy được. Có thể viết tất cả các loại chương trình chỉ với Java SE.</li>
    <li>Java EE - Java Enterprise Edition: xây dựng trên nền Java SE + cung cấp thêm thư viện, môi trường thực thi phục vụ ứng dụng lớn, các dịch vụ trên máy chủ...</li>
    <li>Java ME - Java Micro Edition: tập con của Java SE, được thiết kế cho các thiết bị nhỏ với tài nguyên hạn chế. Trước thời dại smart phone với Android và iOS, hầu như tất cả các điện thoại đều hỗ trợ Java ME.</li>
  </ul>
  <li> Java trên Android: là một platform được thiết kế riêng cho Android, tạm coi nó không phải là Java ME, cũng không phải là Java SE "thuần chủng". Các phiên bản Android trước đây dựa trên Apache Harmony, sau này dựa trên Open JDK.</li>
 </ul>

Tiếp theo là về JDK, JRE, JVM  
Nguồn tìm hiểu:
<ul>
  <li><a href="https://www.geeksforgeeks.org/differences-jdk-jre-jvm/">Differences between JDK, JRE and JVM - GeeksforGeeks</a></li>
  <li><a href="https://stackoverflow.com/questions/1906445/what-is-the-difference-between-jdk-and-jre">What is the difference between JDK and JRE? - Stackoverflow</a></li>
  <li><a href="https://viettuts.vn/java/su-khac-nhau-giua-jdk-jre-va-jvm">Sự khác nhau giữa JDK, JRE và JVM - Viettuts</a></li>
</ul>  
Ngắn gọn thì chỉ cần nhìn hình bên dưới:
<p align="center">
 <img src="https://media.geeksforgeeks.org/wp-content/uploads/JDK_JRE_JVM_x.jpg" alt="ảnh chụp màn hình" width="300">
</p>
<p align="center">
 <i>Nguồn: Differences between JDK, JRE and JVM - GeeksforGeeks</i>
</p>
<ul>
  <li>JVM - Java Virtual Machine - Máy ảo Java: "<i>acts as a run-time engine to run Java applications</i>". Chịu trách nhiệm thực thi chương trình Java từng dòng, như 1 trình thông dịch ??? <a href="https://www.geeksforgeeks.org/jvm-works-jvm-architecture/">Tìm hiểu thêm về cách hoạt động của JVM.</a></li>
  <p align="center">
    <img src="https://media.geeksforgeeks.org/wp-content/uploads/jvm-3.jpg" width="300">
  </p>
  <ul>
    <li>Nhờ có JVM mà chương trình Java được gọi là Write One Run Everywhere</li>
    <li>Về lỗi <i>java.lang.ClassNotFoundException</i>
    <p align="center">
      <img src="https://user-images.githubusercontent.com/61912505/108597585-5f02d880-73bc-11eb-8220-37ae041f99f3.png" width="600">
    </p>
    <li>JVM vs Just-In-Time Compiler(JIT) : JIT là thành phần trong Excecution Engine của JVM. Được sử dụng để tăng hiệu quả của trình thông dịch.</li>
  </ul>
  <li>JRE - Java Runtime Environment: Chứa những gì cần để chạy chương trình Java (đã biên dịch ???). Bao gồm: JVM, core classes, supporting files, lệnh `java`,... Không thể sử dụng để tạo chương trình mới. Nếu chỉ quan tâm đến việc chạy chương trình Java trên máy tính, chỉ cần cài JRE (tức là, chỉ dùng chạy, không dùng để phát triển chương trình).</li>
  <li>JDK - Java Development Kit: SDK (Software Development Kit) đầy đủ tính năng cho Java, là bộ Kit cung cấp môi trường để phát triển và thực thi (chạy) chương trình Java. Gồm: Development Tools(cung cấp mô trường phát triển chương trình Java, như compiler `javac`, tools `jdoc`, `jdb`) và JRE (để chạy chương trình Java). Được sử dụng bởi Java Developers (nghĩa là muốn code Java thì cần cài JDK).</li>
</ul>

---

<div id="2-java-version"></div>

### 2. Java version

Nếu bạn đã từng mông lung trước các phiên bản java như 1.8 và 8... thì chúng ta giống nhau rồi, cùng tìm hiểu nhé. 

Xem thông tin tại 1 số nguồn sau:
<ul>
  <li><a href="https://en.wikipedia.org/wiki/Java_version_history">Lịch sử các phiên bản Java - Wikipedia</a>.</li>
  <li><a href="https://www.quora.com/Do-Java-1-8-and-Java-8-refer-to-the-same-thing">Do Java 1.8 and Java 8 refer to the same thing? - Quora</a></li>
  <li><a href="https://www.oracle.com/java/technologies/javase/jdk8-naming.html">JDK 8 Naming</a>.</li>
</ul>

Nói ngắn gọn và đơn giản thì Java 8 và 1.8 là nhắc tới cùng một thứ. Tương tự có Java 5 ~ Java 1.5, Java 6 ~ 1.6, Java 7 ~ Java 1.7. Còn Java 10, 11, 12, 13, 14... thì không biết :v

Theo <a href="https://en.wikipedia.org/wiki/Java_version_history">Wikipedia</a>:
<ul>
  <li>Ban đầu ta có JDK 1.0 (phiên bản ổn định đầu tiên, JDK 1.0.2 được gọi là Java 1), rồi JDK 1.1</li>
  <li>Sau đó có J2SE 1.2 (Java 2 Platform, Standard Edition - thay từ "JDK" để phân biệt với J2EE, J2ME), rồi J2SE 1.3, J2SE 1.4<li>
  <li>J2SE 5.0
  <ul>
    <li>À, 1 ý nhỏ, Java v1.5.0_05 ta gọi là Java 5 Update 5</li>
    <li>Ở đây giới thiệu 1 hệ thống phiên bản mới cho ngôn ngữ Java. Cả version numbers "1.5.0" và "5.0" được sử dụng để chỉ bản release này của Java 2 Platform Standard Edition. Version "5.0" là product version, còn "1.5.0" là developer version. Con số "5.0" được sử dụng vì "<i>better reflect the level of maturity, stability, scalability and security of the J2SE.</i>". Điều này tiếp tục với các bản phát hành sau đó (Java 6 = JDK 1.6, Java 7 = JDK 1.7,...).
  </ul>
  <li>Java SE 6: Sun thay tên "J2SE" bằng "Java SE" và bỏ ".0" khỏi version number. Nhưng số 1.6.0 thì vẫn là 1.6.0.</li>
  <li>Rồi thì Java SE 7, Java SE 8 (LTS - Long-Term Support), 9, 10, 11 (LTS), 12, 13, 14....
</ul>

Oke done.












 
