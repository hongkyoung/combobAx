# jQuery Accessible combobox plugin

웹접근성을 준수하며, 폼 컨트롤이 가능한 제이쿼리 콤보박스(셀렉트박스) 플러그인

- Current version: 0.1.1
- Release: 2016. 04. 04

## 데모

<a target="_blank" href="http://www.choigyumin.com/_view/jquery.accessiblecombobox/">http:&#47;&#47;www.choigyumin.com&#47;_view&#47;jquery.accessiblecombobox&#47;</a>

## 다운로드

<a target="_blank" href="https://github.com/choi4450/jquery.accessiblecombobox/tree/master/dist">https:&#47;&#47;github.com&#47;choi4450&#47;jquery.accessiblecombobox&#47;tree&#47;master&#47;dist</a>

## 기능

- &lt;select&gt;태그를 쉽게 디자인을 커스터마이징할 수 있는 HTML 구조로 변경하며 기본적인 인터랙션 제공
- &lt;option&gt;태그를 &lt;li&gt;, &lt;a&gt;태그가 아닌 &lt;input type="radio"&gt;태그로 표현함으로써 웹접근성을 준수
    - &lt;input type="radio"&gt;태그의 접근성을 해치지 않는 선에서 &lt;select&gt;태그와 유사한 키보드 접근성 제공
- form 컨트롤 가능
- IE7 지원

## 사용 방법

### Handler

#### HTML

```html
<select id="f-cbo" name="example" title="Example" aria-label="Example" style="width:250px" class="example" data-accessiblecbo="label: '다른 옵션 선택'">
    <option value="A">Option A</option>
    <option value="B">Option B</option>
    <option value="C">Option C</option>
</select>
```

#### JavaScript

```javascript
$('.example').each(function() {
    $(this).accessibleCombobox({
        label: '다른 옵션 선택'
    });
});

// or
$('.example').accessibleCombobox({
    label: '다른 옵션 선택'
});
```

### Initialize

```javascript
{
    label: 'Select another option',
    bullet: ''
}
```

#### label

버튼을 나타내는 이름(aria-label) 설정

```js
{
    label: '다른 옵션 선택'
}
```

```html
<a href="#" class="accessiblecbo-btn" role="button" aria-live="off" title="Example" aria-label="다른 옵션 선택">
    <span class="accessiblecbo-btn-txt">Option A</span>
    <span class="accessiblecbo-btn-bu" aria-hidden="true"></span>
</a>
```

#### bullet

블릿 아이콘에 추가할 마크업

```js
{
    bullet: '<small>▼</small>'
}
```

```html
<a href="#" class="accessiblecbo-btn" role="button" aria-live="off" title="Example" aria-label="Select another option">
    <span class="accessiblecbo-btn-txt">Option A</span>
    <span class="accessiblecbo-btn-bu" aria-hidden="true"><small>▼</small></span>
</a>
```

## 예정 작업

- 사용자 정의 옵션 제작(애니메이트 외 여러가지)
- <del>Windows XP IE7에서 enter로 radio 선택 시 submit 방지</del>
