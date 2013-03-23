<p>ASIHTTPRequest-no-arc
  </p>
<p>=====================  </p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>非自动释放内存版本
  
  
  
  
  
  安装类库  </p>
<p>=====================  </p>
<p>SystemConfiguration.framework</p>
<p>MobileCoreServices.framework  </p>
<p>CoreGraphics.framework  </p>
<p>libz.1.2.3.dylib  </p>
<p>libxml2.dylib  </p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>其它  </p>
<p>=====================  </p>
<p>导入了libxml2.dylib，但是却提示libxml/HTMLparser.h file not found，那是因为你的开发环境默认的路径无法找到这个libxml2.dylib框架，修改方法：
  
  （两种方法都试一下吧）  </p>
<p>第一种方法：
  点击左边项目的根目录，再点击右边的Build Settings，手工输入文字：“Header search paths”，然后单击（或双击，点击弹出面板下面的“+”号进行添加）“Header search paths ”右边的空白处，输入：/usr/include/libxml2  </p>
<p>如果还不行，试试这个方法：
  点击左边项目的根目录，再点击右边的Build Settings，手工输入文字：“Header search paths”，然后单击（或双击，点击弹出面板下面的“+”号进行添加）“ Header search paths ”右边的空白处，输入：${SDK_DIR}/usr/include/libxml2 </p>
<p>&nbsp;</p>
<p>&nbsp;</p>
