# 0903 관통 프로젝트 



	### 구조

![list](.\list.JPG)

​	pjt04 프로젝트 - movies app 

​		- gitignore추가.

​		- 부트스트랩이 아닌 CSS 파일을 만들어 적용해 봄.

​		- requirement.txt 추가.



---



### 구현 순서

​	1) 우선 프로젝트 README 파일을 보고 전체 구조를 파악한 후 urls, views, templates 순으로 작성.

​	2) 이 후 레이아웃을 보고 CSS파일을 추가.

​	3) 업로드 시 필요없는 부분 gitignore 추가.



---



### 문제

​	1) 전체적인 개념과 순서는 여러 수업을 통해 익숙했지만 세부적인 import, 터미널 명령어 등의 숙지 부족.

​	2) 진행 중, views 파일에서 프로그램을 구성할 때 어디로 redirect할지 헷갈렸다.

​	3) Django에서 CSS, JS 연결의 다른점, block 구조로 CSS를 파일의 어느부분에 + 어떻게 적용할 지 혼란.



---



### 학습내용

​	1) pjt04/urls.py

``` python
urlpatterns = [
    path('admin/', admin.site.urls),
    path('articles/', include('articles.urls', namespace='articles')),
]
```

​		namespace 오류가 난 적이 있었는데 앱폴더 urls 에 app_name=~~~, 프로젝트 폴더 urls / include 두 번째 

​		인자로 namespace='~' 로 작성하니 해결 됨. 이유를 모르겠습니다. ㅜ



 	2) CSS 적용

​			html에 보통 asset 폴더에 파일을 추가한 후 link로 바로 연결할 수 있었던 반면. 장고에서는 setting.py에 

​			static 관련 설정을 해줘야 하고(BASE static경로 설정, impore os 등등), html파일에도 import static 을 작

​			성해주고 적용해야 했다. 

​	

