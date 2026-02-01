# D017  vue+django+neo4j音乐知识图谱推荐可视化分析系统|带管理员角色+爬虫

> 完整项目收费，可联系QQ: 81040295 微信: mmdsj186011 注明从git来的，谢谢！
也可以关注我的B站： 麦麦大数据 https://space.bilibili.com/1583208775
> 

up主B站：  **麦麦大数据**
关注B站，有好处！
编号:  D017
## 视频

[video(video-A9liVAlX-1758701391257)(type-bilibili)(url-https://player.bilibili.com/player.html?aid=521223603)(image-https://i-blog.csdnimg.cn/img_convert/96aa37acef8d322c28583b9542adefb5.png)(title-D17vue+django 音乐推荐大数据系统源码|协同过滤推荐算法|多角色| mysql | 爬虫|)]

## 1 系统简介
系统简介：本系统是一个基于Vue+Django+Neo4j+MySQL构建的音乐推荐系统，旨在为用户提供个性化的音乐推荐服务。其核心功能围绕音乐推荐、数据可视化、用户管理和系统权限管理展开。主要包括：首页，用于展示系统概览和推荐内容；音乐推荐模块，通过基于用户的协同过滤和基于物品的协同过滤的混合推荐算法，提供个性化的音乐推荐服务；数据可视化模块，通过图表展示用户行为数据、音乐流行趋势和用户偏好分析；知识图谱可视化，展示用户与歌曲、歌手之间的关联关系；以及用户管理模块，包含登录、注册、权限管理和个人设置功能，确保系统的安全性和个性化体验。
## 2 功能设计
该系统采用典型的B/S（浏览器/服务器）架构模式。用户通过浏览器访问Vue前端界面，前端由HTML、CSS、JavaScript以及Vue.js生态系统中的Vuex（用于状态管理）、Vue Router（用于路由导航）和Echarts（用于数据可视化）等组件构建。前端通过API请求与Django后端进行数据交互，Django后端则负责业务逻辑处理，并与MySQL数据库和Neo4j图数据库进行交互。MySQL数据库主要用于存储结构化数据，如用户信息、歌曲信息、歌手信息等，而Neo4j图数据库则用于存储和查询用户与歌曲、歌手之间的关联关系，支持知识图谱的可视化功能。此外，系统还包含一个独立的爬虫模块，负责从外部来源抓取歌曲、歌手和专辑数据，并将其导入MySQL和Neo4j数据库，为整个系统提供数据支撑。
### 2.1系统架构图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/78a8e25a02f944a1a1280040241059fa.png)
### 2.2 功能模块图
用户功能模块：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/659a082935954c1eb59e38bd020e77e1.png)

管理员功能模块：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/69e6faf6e91b4adaaac3d7871d11074f.png)
### 2.3 文档 17000字
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0d3658da338d4b0d8d7af4f5db938fb3.png)
### 2.4 目录
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9e1b44647edc4fb2918d6e0b2a049b10.png)
## 3 功能展示
### 3.1 登录 & 注册
登录界面背景是一个视频，展示和本文系统主题相匹配的内容，登录和注册界面在一个界面下，通过按钮来切换，注册界面输入用户名和密码，会检查这个用户是否存在，登录界面则要检查用户名是否存在以及用户名密码是否正确：  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9b4f755457d04b98ab751e93a2bcac63.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d13b6f145ef04bfe8e725814a6a85cbc.png)
### 3.2 主页
如果通过校验，则可以进入主页，在主页是一个左侧菜单，右侧操作面板的布局，右上角是登录用户的头像和退出按钮
系统主要可以分为两个角色：用户和管理员，下面分别从两个不同角色来进行功能的展示
### 3.3 歌曲推荐 【用户端】
- 提供系统的入口，展示推荐内容，例如通过user-based CF和item-based CF的混合推荐。
- 通过引导用户，方便他们快速找到感兴趣的音乐。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b65877ef3c974895b36de38b7fd5ac2a.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/550fc0ad04d8478ab2e1f64998c98477.png)
### 3.4 **大屏分析**【用户端】
- 提供数据仪表盘，展示用户的使用情况、音乐播放频率等关键信息。
- 通过数据透视，帮助用户更好地理解其音乐趣味及使用习惯。
数据大屏实现：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/fe67cbc9b8be4bb2b056f05e6d4c17e5.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5afca5cde2644eff94fc6d8ccdac2f52.png)
### 3.5 **歌曲歌手数据可视化分析**【用户端】
- 分析和展示当前流行歌曲的趋势、评分和受欢迎程度。
- 为用户提供有价值的参考，帮助他们发现新音乐。
版权分析：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/17a8965ae436483e88dd53c053718678.png)
热度分析：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e526ae153ca645b9b7a1acd33b43ddc1.png)
热门发行分析：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/91fd46dc246849fab510d707ee3352a9.png)
### 3.6 **词云分析**【用户端】
- 根据用户听的歌曲或评论生成词云，直观呈现用户的音乐偏好。
- 增强趣味性和互动性，提升用户体验。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/56722c3657dd4980a52d2df713d5790e.png)
### 3.7 **知识图谱可视化**【用户端】
- 通过图形化展示用户与歌曲、歌手之间的关联，增加音乐信息的可访问性。
- 有助于用户发现潜在的音乐连接，提升用户的探索乐趣。
- 基于neo4j 图数据库加以实现，前端使用echarts实现可视化。
neo4j知识图谱实现：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5ce5562f5f2b403a83324014d3ac5840.png)
本系统知识图谱可视化：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d040fbf5812e4fd39f058ea4b4efad3d.png)
知识图谱检索：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4a0552c1c89e4a8cbd286e80f3689fed.png)
### 3.8 **歌曲点赞**【用户端】
- 用户可以对喜欢的歌曲进行点赞，增强用户的互动性。
- 收集用户对歌曲的反馈，为后续的推荐算法提供数据支持。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b5d66ba32d274a9ca5db807aec736820.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/99a7999829b645f18c94fbbe87e2dfa2.png)
### 3.9 **权限管理**【管理员端】
- 实现对用户和管理员的权限控制，确保系统中的数据和功能安全符合预设的访问规则。
- 可以设置不同级别的用户权限，确保管理人员能够进行更高级别的操作，同时限制普通用户的功能访问。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1f64bd18b0b54a41b73e2a6136238463.png)
### 3.10 **用户管理**【管理员端】

- 可对用户信息进行增删改查操作，便于管理员管理用户。
- 可以追踪用户的活动记录，为个性化推荐提供数据支持。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/91cbae73981c4c798f2413665390bf22.png)
### 3.11 **歌曲管理**【管理员端】

- 管理系统中的歌曲列表，包括添加、编辑和删除歌曲信息。
- 确保歌曲数据的及时更新和准确性，为推荐系统提供最新的音乐内容。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/026f2e7693144812960a51486e8cc88a.png)
### 3.12 **歌手管理**【管理员端】
- 对歌手信息进行维护，包括添加、新增和编辑歌手资料。
- 提供给用户更全面的音乐信息，增强用户的使用体验。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8608b83941254cfa81ced565b0d1e982.png)
### 3.13 **管理员管理**【管理员端】
- 管理员的账户管理功能，包括权限分配、信息维护等。
- 保障系统的安全性，保证只有授权人员可以进行访问和操作。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ede97505e5da41378448d55e74556809.png)
### 3.14 个人设置
个人设置方面包含了**用户信息修改**、**密码修改**功能。
用户信息修改中可以上传头像，完成用户的头像个性化设置，也可以修改用户其他信息。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/615a99be42b741afb2810b9afd8b6cd9.png)
修改密码需要输入用户旧密码和新密码，验证旧密码成功后，就可以完成密码修改。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/252e0a9ded9a4250ac7749b40e5a2453.png)
### 3.15 歌曲爬虫
通过爬虫获取歌曲、歌手和专辑的数据
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/94644c89ef894faf818b6576d7fc480a.jpeg)
## 4程序代码
### 4.1 代码说明
代码介绍：代码实现了基于UserCF的推荐算法，主要包括以下部分：
数据模型定义：包括用户、物品和用户评分的模型。
recommendation.py：核心算法实现，包括相似性矩阵计算和推荐生成。
views.py：Django视图，处理推荐请求并返回结果。
流程图展示了从数据收集到推荐结果的完整流程。推荐算法通过计算用户间的相似度，找到相似用户，然后根据相似用户的评分生成推荐列表。
### 4.2 流程图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c9d9df2fe28744efa0fb9699053bbd3e.png)

### 4.3 代码实例
```python
# models.py
from django.db import models

class User(models.Model):
    id = models.AutoField(primary_key=True)
    username = models.CharField(max_length=50)

class Item(models.Model):
    id = models.AutoField(primary_key=True)
    title = models.CharField(max_length=100)

class UserItemRating(models.Model):
    user = models.ForeignKey(User, on_delete=models.CASCADE)
    item = models.ForeignKey(Item, on_delete=models.CASCADE)
    rating = models.IntegerField(default=0)

# recommendation.py
from django.db.models import Q
from sklearn.metrics.pairwise import cosine_similarity
import numpy as np

def compute_similarity_matrix(user_ids, item_ids, ratings):
    """构建用户-物品评分矩阵并计算相似性"""
    matrix = np.zeros((len(user_ids), len(item_ids)))
    for i, user_id in enumerate(user_ids):
        for j, item_id in enumerate(item_ids):
            try:
                rating = UserItemRating.objects.get(user=user_id, item=item_id).rating
                matrix[i][j] = rating
            except:
                matrix[i][j] = 0
    return cosine_similarity(matrix)

def get_recommendations(user_id, num_recs=5):
    """基于UserCF算法获取推荐列表"""
    similar_users = compute_similar_users(user_id)
    recommended_items = {}
    for user in similar_users:
        user_ratings = UserItemRating.objects.filter(user=user).exclude(item__in=recommended_items.keys())
        for rating in user_ratings:
            if rating.item.id not in recommended_items:
                recommended_items[rating.item.id] = 0
            recommended_items[rating.item.id] += rating.rating
    sorted_items = sorted(recommended_items.items(), key=lambda x: x[1], reverse=True)[:num_recs]
    return [Item.objects.get(id=item[0]) for item in sorted_items]

def compute_similar_users(user_id, top_n=10):
    """计算与目标用户最相似的前N个用户"""
    user_ids = list(User.objects.values_list('id', flat=True))
    ratings = []
    for user in user_ids:
        user_ratings = UserItemRating.objects.filter(user=user)
        ratings.append([rating.rating for rating in user_ratings])
    similarity = compute_similarity_matrix(user_ids, user_ids, ratings)
    similar_indices = np.argsort(-similarity[user_id])[:top_n]
    return [user_ids[i] for i in similar_indices]

# views.py
from django.http import JsonResponse
from .recommendation import get_recommendations

def recommend(request, user_id):
    recommended_items = get_recommendations(user_id)
    results = [{'id': item.id, 'title': item.title} for item in recommended_items]
    return JsonResponse({'recommendations': results})

```

---
## 联系方式
