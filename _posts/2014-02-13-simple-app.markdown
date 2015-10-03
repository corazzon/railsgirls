---
layout: default
title: Simpler Rails Girls App Tutorial
permalink: simpleapp
---

# 레일스 걸스 앱 튜토리얼

*Created by Vesa Vänskä, [@vesan](https://twitter.com/vesan)*

*Edited to include [simple_scaffold](https://github.com/Ben-M/simple_scaffold) by Ben Maraney.*

**미리 레일스를 설치해야 합니다.** [**설치 가이드 링크로 가서**](../install) 참고하세요.


## 툴을 살펴봅니다.

<div class="indent" markdown="1">

<h3><i class="icon-text-editor">&nbsp;</i></h3>

<h3>텍스트 에디터</h3>

<p><a href="http://www.sublimetext.com">서브라임 텍스트</a>, <a href="http://www.activestate.com/komodo-edit">코모도 에디트</a>, 빔, 이맥스, 지에디트는 코드를 편집하는 대표적인 텍스트 에디터입니다.</p>

<h3><i class="icon-prompt">&nbsp;</i></h3>

<h3>터미널 (윈도우즈에서 명령행 프롬프트)</h3>
에서 레일스를 서버로 실행하고 명령어를 실행합니다.

<h3><i class="icon-browser">&nbsp;</i></h3>

<h3>웹브라우저</h3>
(파이어폭스, 사파리, 크롬) 여러분이 만든 애플리케이션을 보여줍니다.

</div>

### Important

여러분이 사용하는 컴퓨터의 운영체제에 따라 안내사항을 선택하도록 합니다. - 윈도우즈 커뮤터에서 실행하는 명령어는 맥과 리눅스와 다릅니다. 따라하면서 실행할 명령어 테두리 아래에서 운영체제를 윈도우즈와 기타 중에서 선택할 수 있습니다.

## *1.*Creating the application

레일스 앱 이름을 *railsgirls*으로 새로 만들겠습니다.

먼저, 터미널을 열겠습니다:

* 맥: 스포트라이트를 열어 *Terminal* 를 키보드로 입력하고 *Terminal* 애플리케이션이 나타나면 선택합니다.
* 윈도우즈: 시작버튼을 눌러 *Command Prompt* 찾아서 *Command Prompt with Ruby on Rails*를 클릭합니다.
* 리눅스 (우분투/페도라): 대시에서 *Terminal*를 찾아서 *Terminal*를 클릭합니다.

다음, 터미널에서 아래와 같이 명령어를 키보드로 입력합니다:

<div class="os-specific">
  <div class="nix">
{% highlight sh %}
mkdir projects
{% endhighlight %}

    <div>
<code>projects</code>라는 이름의 디렉토리가 있는지 확인하려면 list 명령어를 실행합니다: <code>ls</code>. <code>projects</code>라는 디렉토리를 화면에 출력됩니다. 그럼 위치를 <code>projects</code> 폴더로 이동하겠습니다:
    </div>

{% highlight sh %}
cd projects
{% endhighlight %}

    <div>
<code>ls</code> 명령어를 실행해보면 디렉토리가 비어있습니다. 그럼 아래와 같이 <code>railsgirls</code> 라는 이름으로 앱을 새로 만들겠습니다:
    </div>

{% highlight sh %}
rails new railsgirls -m http://railsgirls.com/simple_scaffold.rb
{% endhighlight %}

    <div>
        <code>rails new railsgirls</code> 실행결과 레일스는 railsgirls 라는 이름으로 프로젝트를 생성하고 프로젝트에 필요한 모든 파일을 생성합니다.
    </div>
    <div>
        <code>-m http://railsgirls.com/simple_scaffold.rb</code> 실행결과 레일스는 템플릿 파일을 railsgirls.com에서 가져와서 초심자가 이해하기에 쉬운 간단한 코드를 만듭니다.
    </div>
    <div>
명령어 실행 결과 <code>railsgirls</code> 폴더에 앱을 새로 만듭니다. 레일스 앱 폴더로 이동하겠습니다:
    </div>

{% highlight sh %}
cd railsgirls
{% endhighlight %}

    <div>
이동한 디렉토리에서 <code>ls</code> 명령어를 실행하면 <code>app</code>과  <code>config</code> 폴더가 있습니다. 레일스를 서버로 실행합니다:
    </div>

{% highlight sh %}
rails server
{% endhighlight %}
  </div>

  <div class="win">
{% highlight sh %}
mkdir projects
{% endhighlight %}

    <div>
<code>projects</code>라는 이름의 디렉토리가 있는지 확인하려면 list 명령어를 실행합니다: <code>dir</code>. <code>projects</code>라는 디렉토리를 화면에 출력됩니다. 그럼 위치를 <code>projects</code> 폴더로 이동하겠습니다:
    </div>

{% highlight sh %}
cd projects
{% endhighlight %}

    <div>
<code>dir</code> 명령어를 실행해보면 디렉토리가 비어있습니다. 그럼 아래와 같이 <code>railsgirls</code> 라는 이름으로 앱을 새로 만들겠습니다:
    </div>

{% highlight sh %}
rails new railsgirls -m http://railsgirls.com/simple_scaffold.rb
{% endhighlight %}

    <div>
        <code>rails new railsgirls</code> 실행결과 레일스는 railsgirls 라는 이름으로 프로젝트를 생성하고 프로젝트에 필요한 모든 파일을 생성합니다.
    </div>
    <div>
        <code>-m http://railsgirls.com/simple_scaffold.rb</code> 실행결과 레일스는 템플릿 파일을 railsgirls.com에서 가져와서 초심자가 이해하기에 쉬운 간단한 코드를 만듭니다.
    </div>
    <div>
명령어 실행 결과 <code>railsgirls</code> 폴더에 앱을 새로 만듭니다. 레일스 앱 폴더로 이동하겠습니다:
    </div>

{% highlight sh %}
cd railsgirls
{% endhighlight %}

    <div>
이동한 디렉토리에서 <code>dir</code> 명령어를 실행하면 <code>app</code>과  <code>config</code> 폴더가 있습니다. 레일스를 서버로 실행합니다:
    </div>

{% highlight sh %}
ruby bin\rails server
{% endhighlight %}
  </div>
</div>

**윈도우즈 사용자:** 레일스를 설치한 버전에 따라서 `bin\rails` 대신 `script\rails`를 실행해야합니다.

브라우저 주소창에 [http://localhost:3000](http://localhost:3000) 입력합니다. "Welcome aboard" 페이지가 나타납니다. 새로운 앱을 오류없이 만들었습니다.

레일스 서버를 실행하였기 때문에 터미널에서 깜빡이는 프롬프트가 사라졌습니다. 아래와 같이 보입니다:

<div class="os-specific">
  <div class="nix">
{% highlight sh %}
$
{% endhighlight %}
  </div>
  <div class="win">
{% highlight sh %}
>
{% endhighlight %}
  </div>
</div>

명령행 프롬프트가 보이지 않아서 다른 명령어를 실행할 수 없습니다. `cd` 명령어를 실행해봐도 꿈쩍하지 않습니다. 정상으로 돌아가려면 다음과 같이 합니다:

터미널에서 `CTRL-C` 를 치고 서버를 종료합니다.

**Coach:** 명령어를 하나씩 설명하세요. 실행결과 무엇을 만들었나요? 서버가 무엇을 하나요? 특별한 템플릿 몇가지는  [GitHub](https://github.com/Ben-M/simple_scaffold)에서 참고하세요.

## *2.*Create Idea scaffold

이번에는 아이디어(idea)를 대상으로 아이디어 전체 목록을 나열하고 추가 삭제 수정하고, 아이디어 하나를 보여주는 코드를 한번에 만들어주는 레일스 스캐폴딩을 사용하겠습니다.

**Coach:** 레일스 스캐폴딩은 무엇인가요? (명령어, 모델 이름, 데이터베이스 테이블, 이름을 짓는 규칙, 속성과 타입 등을 설명합니다.) 마이그레이션은 무엇이고 마이그레이션이 왜 필요한가요?

<div class="os-specific">
  <div class="nix">
{% highlight sh %}
rails generate scaffold idea name:string description:text picture:string
{% endhighlight %}
  </div>

  <div class="win">
{% highlight sh %}
rails generate scaffold idea name:string description:text picture:string
{% endhighlight %}
  </div>
</div>

스캐폴드는 프로젝트 디렉토리에서 파일을 새로 만듭니다. 하지만 제대로 동작하려면 명령어를 몇개를 실행하여 데이터베이스를 업데이트하고 서버를 재시작해야합니다.

<div class="os-specific">
  <div class="nix">
{% highlight sh %}
rake db:migrate
rails server
{% endhighlight %}
  </div>

  <div class="win">
{% highlight sh %}
rake db:migrate
ruby bin\rails server
{% endhighlight %}
  </div>
</div>

브라우저 주소창에  [http://localhost:3000/ideas](http://localhost:3000/ideas) 입력합니다. 화면에 보이는 아무 링크나 클릭해보고 실행결과를 봅니다.

`CTRL-C` 쳐서 서버를 종료합니다.


## *3.*Design

**Coach:** HTML과 레일스의 관계를 설명하세요. 뷰에서 HTML는 어느 파트이고 임베디드 루비(ERB)는 무엇인가요? MVC는 무엇이고 서로 어떤 관련이 있나요?(모델과 컨트롤러가 HTML 뷰를 생성하는데 맡은 역할)

앱은 아직까지 밋밋해보입니다. 좀 꾸며보겠습니다. 트위터 부트스트랩 프로젝트를 사용하여 매우 쉽게 프로젝트를 꾸며보겠습니다.

텍스트 에디터로 `app/views/layouts/application.html.erb` 파일을 편집합니다.

{% highlight erb %}
<%= stylesheet_link_tag "application", media: "all", "data-turbolinks-track" => true %>
{% endhighlight %}

줄 위에 

{% highlight erb %}
<link rel="stylesheet" href="//railsgirls.com/assets/bootstrap.css" />
<link rel="stylesheet" href="//railsgirls.com/assets/bootstrap-theme.css" />
{% endhighlight %}

를 넣고 아래와 같은 줄을 

{% highlight erb %}
<%= yield %>
{% endhighlight %}

다음과 같이 

{% highlight erb %}
<div class="container">
  <%= yield %>
</div>
{% endhighlight %}

수정합니다. 레이아웃에 네비게이션 바와 푸터를 붙이겠습니다. `<body>` 태크 아래에 

{% highlight html %}
<nav class="navbar navbar-default navbar-fixed-top" role="navigation">
  <div class="container">
    <div class="navbar-header">
      <button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
      <a class="navbar-brand" href="/">The Idea app</a>
    </div>
    <div class="collapse navbar-collapse">
      <ul class="nav navbar-nav">
        <li class="active"><a href="/ideas">Ideas</a></li>
      </ul>
    </div>
  </div>
</nav>
{% endhighlight %}

와 같이 넣고 `</body>` 태그를 닫기 전에

{% highlight html %}
<footer>
  <div class="container">
    Rails Girls 2013
  </div>
</footer>
<script src="//railsgirls.com/assets/bootstrap.js"></script>
{% endhighlight %}

넣습니다. 그럼 아이디어 테이블도 꾸미겠습니다. `app/assets/stylesheets/application.css` 파일을 아래와 같이 수정합니다.

{% highlight css %}
body { padding-top: 100px; }
footer { margin-top: 100px; }
table, td, th { vertical-align: middle !important; border: none !important; }
th { border-bottom: 1px solid #DDD !important; }
{% endhighlight %}

파일을 저장하고 브라우저의 새로고침 버튼을 누르면 수정한 내용이 나타납니다. HTML과 CSS를 좀 더 바꿀 수 있습니다.

**Coach:** CSS와 레이아웃에 대해 간략히 설명하세요.


## *4.*Adding picture uploads

레일스에 파일을 업로드하려면 소프트웨어 몇개를 설치해야 합니다.

프로젝트 디렉토리에서 `Gemfile` 이라는 파일을 텍스트 에디터로 아래와 같이 수정합니다.

{% highlight ruby %}
gem 'sqlite3'
{% endhighlight %}

아래 줄에 다음과 같이 젬을 추가합니다.

{% highlight ruby %}
gem 'carrierwave'
{% endhighlight %}

**Coach:** 라이브러리가 무엇이고 왜 유용한지 설명하세요. 오픈 소스 소프트웨어를 설명하세요.

터미널에서 아래와 같이 실행합니다:

{% highlight sh %}
bundle
{% endhighlight %}

그런 다음 업로드를 처리하는 코드를 짜겠습니다. 터미널에서 아래와 같이 실행합니다:

{% highlight sh %}
rails generate uploader Picture
{% endhighlight %}

**레일스 서버를 재시작**합니다.

터미널에서 `CTRL-C` 쳐서 서버를 종료합니다. 종료하면 윗방향 화살표를 누르면 최근에 실행한 명령어가 나타납니다. 최근 명령어로 서버를 재시작할 수 있습니다.

재시작해야 앞서 추가한 라이브러리를 사용할 수 있습니다.

`app/models/idea.rb` 파일을 수정합니다. 

{% highlight ruby %}
class Idea < ActiveRecord::Base
{% endhighlight %}

줄 아래에 

{% highlight ruby %}
mount_uploader :picture, PictureUploader
{% endhighlight %}

와 같이 추가합니다. `app/views/ideas/_form.html.erb` 파일을 수정합니다. 

{% highlight erb %}
<%= f.text_field :picture %>
{% endhighlight %}

를 아래와 같이 

{% highlight erb %}
<%= f.file_field :picture %>
{% endhighlight %}

바꿉니다. 어쩌면, *TypeError: can't cast ActionDispatch::Http::UploadedFile to string* 에러가 발생할 수 있습니다.

이런 경우, `app/views/ideas/_form.html.erb` 파일을 수정합니다.

{% highlight erb %}
<%= form_for(@idea) do |f| %>
{% endhighlight %}

를 아래와 같이 

{% highlight erb %}
<%= form_for @idea, :html => {:multipart => true} do |f| %>
{% endhighlight %}

바꿉니다. 브라우저에서 아이디어에 사진을 넣을 수 있습니다. 사진 파일을 업로드해보면 사진이 안보이고 파일 위치만 보입니다. 사진이 보이도록 수정하겠습니다.

`app/views/ideas/show.html.erb` 파일을 수정합니다.

{% highlight erb %}
<%= @idea.picture %>
{% endhighlight %}

를 아래와 같이 

{% highlight erb %}
<%= image_tag(@idea.picture_url, :width => 600) if @idea.picture.present? %>
{% endhighlight %}

바꿉니다. 브라우저의 새로고침 버튼을 눌르면 사진이 보입니다.

**Coach:** HTML를 간략히 설명하세요.


## *5.*Finetune the routes

브라우저에서 <http://localhost:3000> (클라우드 서비스를 사용하면 미리보기 주소)로 이동합니다. 첫 페이지가 "Welcome aboard"가 보이는데 첫 페이지를 아이디어 페이지가 보이도록 바꾸겠습니다. 

`config/routes.rb` 파일을 수정합니다. 첫번째 줄에 아래와 같이 추가합니다.

{% highlight ruby %}
root :to => redirect('/ideas')
{% endhighlight %}

브라우저에서 루트 패스(<http://localhost:3000/> 또는 미리보기 주소)를 열어서 수정한 내용을 확인합니다.

**Coach:** 라우트를 설명합니다. 스태틱 파일의 관계와 라우트 순서를 포함하여 설명합니다.

**Rails 3 users:** `/public/` 디렉토리의 index.html 파일을 삭제해야 합니다.

## Create static page in your app

애플리케이션를 만든 사람을 소개하는 정보를 담은 스태틱 페이지를 만들겠습니다!

{% highlight sh %}
rails generate controller pages info
{% endhighlight %}

위의 명령어 실행결과 `app/views` 폴더 아래에 `pages` 폴더와 그 아래에 소개 정보를 넣을 `info.html.erb` 파일을 생성합니다.

그리고 routes.rb 파일에 아래와 같이 추가됩니다.

{% highlight ruby %}
get "pages/info"
{% endhighlight %}

`app/views/pages/info.html.erb` 파일에 HTML로 여러분에 대해 정보를 넣습니다. 새로 만든 페이지를 보려면,  [http://localhost:3000/pages/info](http://localhost:3000/pages/info) 브라우저로 이동합니다.

## What next?

* HTML과 CSS로 디자인합니다.
* 평점 매기는 기능을 추가합니다.
* 커피스크립트(자바스크립트)로 화면에서 움직이는 코드를 짭니다.
* 사진 파일 크기를 줄여서 사진이 화면에 빨리 보이도록 수정합니다.


## Additional Guides

* Guide 0: [루비, 레일스, 콘솔에 대한 치트시트](https://github.com/PragTob/rails-beginner-cheatsheet)
* Guide 1: [댓글 달기 Janika Liiv](../commenting)
* Guide 2: [헤로쿠로 배포하기 Terence Lee](../heroku) / [오픈시프트로 배포하기 Katie Miller](../openshift)
* Guide 3: [Build a map of workshop participants by Rails Girls Berlin](http://railsgirlsberlin.de/apptutorial/)
* Guide 4: [썸네일 이미지 만들기 Miha Filej](../thumbnails)
* Guide 5: [HTML과 CSS 디자인 Alex Liao](../design)
* Guide 6: [디바이즈 젬을 사용하여 인증(사용자 계정)하기 Piotr Steininger](../devise/)
* Guide 7: [위에서 만든 레일스 걸스 애플리케이션을 단계별로 설명 Lucy Bain](https://github.com/lbain/railsgirls)

