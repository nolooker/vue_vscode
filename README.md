# vue_vscode

    - npm install -g @vue/cli

    - Vetur / HTML CSS Support / Vue 3 Snippets / Vue Language Features (Volar) 설치
        => vue3.x에서는 Vetur 대신 Volar 권장
        why? => vue2.x까지는 <template>에는 반드시 root element가 하나 있어야 했고, vue3.x에서는 이 제약사항이 풀림

    - vue create vue (yes.then() => Version choice)

    - vue 생성 확인 

    - vue/src/App.vue => html/js/css modify

    - .then(cd vue).then(npm run serve)

        - node_modules : 프로젝트에 쓰는 라이브러리
        - src          : 소스코드 담는 곳
        - public       : html 파일, 기타 파일 보관
        - package.json : 라이브러리 버전, 프로젝트 설정 기록
        
# 데이터바인딩

    - template => {{ x }}
        Because of => No hardcoding && vue auto rendering

    - html 속성 데이터바인딩 => :속성="데이터이름"
        ex) st = 'color : red' => h1 :style="st" /h1

    - v-for 반복 함수

    - js onClick() => Vue.js @click

    - Vue methods:{
        <!-- vue에서 사용할 함수 만드는 경우 사용 -->

        함수 안에서 데이터 쓸 땐 this.x / 반드시 this. 를 붙여줘야 변수 가져옴
    } 