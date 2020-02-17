# Research-on-the-operation-of-knowledge-graph
# 基于知识图谱运态知识点之研究

### 1. Start with a question！ 

如何产生学习顺序，哪些课题是相互关联的?

### 2. Get & Clearn Data 获取数据集

> * **技术**：Scrapy 、MongoDB
> * **范围**： B站
>
> * **数据集**： 分类：科技.演讲.公开课
>
> * **时间范围**：before - 2020/1.：Bilibili公开课

**构建数据结构：**

> - id
> - title 
> - type_hide
> - keyword
> - href
> - time
> - like_on
> - video_list

<table>
  <tr>
   	 <td>id</td>
     <td>title</td>
     <td>type_hide</td>
     <td>keyword</td>
     <td>href</td>
     <td>time</td>
     <td>like_on</td>
     <td>video_list</td>
  </tr>
    <tr>
   	 <td>&nbsp</td>
     <td>&nbsp</td>
     <td>&nbsp</td>
     <td>&nbsp</td>
     <td>&nbsp</td>
     <td>&nbsp</td>
     <td>&nbsp</td>
     <td>&nbsp</td>
  </tr>
</table>

* 数据链接：https://search.bilibili.com/all?keyword=[关键字]
* 视频列表链接（AJAX）：

> * https://api.bilibili.com/x/web-interface/view?aid=[视频av号]
> * https://api.bilibili.com/x/player/pagelist?aid=[视频av号]&jsonp=jsonp

* 视频列表中的api固定为：https://www.bilibili.com/video/[av号]?p=[视频列表中的id]


### 3. Perform EDA(Exploratory-Data-Analysis) 

> * Find top words ,relevant subject            **TF-IDF**
> * *学习词云* （待定）

### 4. Apply Techniques 

> * **分词**
>
> * *情感分析*(待定)
>
> * **主题相似度比较**
>
>   > * **LSI:** [Latent Semantic Indexing 隐式语义索引](https://www.cnblogs.com/mlfighting/archive/2013/04/21/3034337.html)
>   >
>   >   > **如果两个单词之间有很强的相关性，那么当一个单词出现时，往往意味着另一个单词也应该出现(同义词)；反之，如果查询语句或者文档中的某个单词和其他单词的相关性都不大，那么这个词很可能表示的，另外一个意思(比如在讨论互联网的文章中，Apple 更可能指的是Apple公司，而不是水果)  。**
>   >
>   >   
>   >
>   > * **NMF:** [Non-negative Matrix Factorization 非负矩阵分解](https://zhuanlan.zhihu.com/p/27460660) 
>   >
>   >   > **它往往能达到表示信息的局部之间相关关系的效果，从而获得更好的处理结果。**
>
> * **生成学习路线**
>
>   >  生成Data Graph 用户通过Petri-Net构建



### 5.构建三元组

  以Java技术栈为例

> * (Java基础-包含-数据类型)、(Java基础-包含-基本语法)、(Java基础-包含-面向对象)、(Java基础-包含-内存与JVM)
> * （Java数据结构与算法-包含-数据结构）、（Java数据结构与算法-包含-算法）
> * （J2EE web-包含-框架技术）、（J2EE web-包含-容器技术）、（J2EE web-包含-前端技术）
> * （JavaIO与网络-包含-基本IO）、（JavaIO与网络-包含-线程与并发）、（JavaIO与网络-包含-网络开发）
> * （Java项目管理-包含-版本控制工具）
