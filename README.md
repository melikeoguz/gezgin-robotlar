<h3>Gezgin Robotlara Giriş Projeleri</h3>


<ul>

<li>Paket Oluşturup Talker ve Listener Nodeları OLuşturma Modülü</li>
<li>Turtlebot3 için Bir Dünya OLuşturma ve Haritalama İşlemi Modülü</li>
<li>Turtlebot3'yi Belli Noktalar Arasında Hareket Ettirme Modülü</li>
<li>Turtlebot3'yi Engellere Çarptırmadan Otomatik Hareket Ettirme Modülü</li>

</ul>


<h4><code>1- Paket Oluşturup Talker ve Listener Nodeları OLuşturma Modülü</code></h4>

<p style="text-align:justify">Bu proje modülümüzdeki amacımız nodelar arasında iletişimi sağlamak ve roscore kapsamında gerçekleşen olayları graph üzerinde görüntülemektir. En önemli kısım ise çalışan node ya da düğümü komut satırı ile konusunu ve adını değiştirebilmekti. Bu proje kapsamında yapılan işlemler aşağıdaki görseller ile birlikte anlatılmaktadır.</p>

<ul>
<li>Öncelikle <code>catkin_create_pkg m_170201028 std_msgs rospy roscpp</code> yazarak bir paket oluşturdum.</li>

<li>Oluşturulan bu paketi <code>catkin_make</code> diyerek derledim.</li>
<li><code>wget https://raw.github.com/ros/ros_tutorials/kinetic-devel/rospy_tutorials/001_talker_listener/talker.py</code> <br/><br/> ve <code>wget https://raw.github.com/ros/ros_tutorials/kinetic-devel/rospy_tutorials/001_talker_listener/listener.py</code> kodlarını yazarak listener ve talker nodelarımın kodlarını açık kaynaklı kodlardan yararlanarak indirdim. </li>
<li><code>chmod +x talker.py</code> ve <code>chmod +x listener.py</code> komutlarını yazarak kodlara yetkilendirme işlemi yaptım.</li>
<li>Bundan sonra yapılması gereken 2 şey kalmıştı. 1) CMakeList içini değiştirmek, 2) package.xml içini değiştirmekti. </li>
<li>CMakeList'i görüntülemek için <a href="https://artemiseticaret.com/wp-content/uploads/2021/01/CMakeLists.txt">buraya</a> basabilirsiniz.</li>
<ul>
<br/>

<img src="https://i.hizliresim.com/gwWyf5.png">
<ul>

<li>roscore komutu ile öncelikle rosu başlatıyoruz.</li>
<li>rosrun m_170201028 talker.py chatter:=/yeni_konu

rosrun m_170201028 listener.py chatter:=/yeni_konu

rosrun m_170201028 talker.py __name:=yeni_melike

rosrun m_170201028 listener.py __name:=yeni_oguz

</ul>

yazarak nodeları başlatalım.

<img src="https://i.hizliresim.com/Al6YRx.png">

Son olarak rqt_graph, rosnode info rosnode list komutlarını kullanarak yaptığımız işlemleri görüntüleyebilirsiniz.

<img src="https://i.hizliresim.com/e087V3.png">
<img src="" >

