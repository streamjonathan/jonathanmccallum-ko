---
title: "아티스트 추천하기"
slug: suggest-an-artist
---

예수님을 따르는 음악가나 아티스트 이야기를 듣는 걸 정말 좋아해요. 제가 글을 쓰거나, 인터뷰하거나, 리액션 영상을 만들면 좋을 사람이 있다면 여기서 알려 주세요.

이름과 링크 하나면 충분해요. 그리고 왜 그 사람인지 한두 마디만 덧붙여 주세요. 보내 주신 건 모두 직접 읽어요. 정말 고마워요.

아는 사람이 있나요? 사진을 누르면 양식이 자동으로 채워져요. 그다음 왜 그 사람인지 한두 마디만 적고 보내 주세요.

<div class="suggest-carousel" role="list" aria-label="추천할 수 있는 음악가와 아티스트">
{% for artist in suggest_carousel %}
  <button type="button" class="suggest-pick" role="listitem" data-artist="{{ artist.name }}" data-link="{{ artist.profile }}" title="{{ artist.name }} 추천하기">
    <img src="{{ artist.img }}" alt="{{ artist.name }}" loading="lazy" width="150" height="150">
    <span class="suggest-pick__name">{{ artist.name }}</span>
    <span class="suggest-pick__note">{{ artist.note }}</span>
  </button>
{% endfor %}
</div>

<p class="suggest-carousel__more">아니면 아래에서 새로운 사람을 추천해 주세요. 제가 꼭 들어야 한다고 생각하는 분이라면 누구든 좋아요.</p>

이 사이트는 18세 미만인 분들을 위한 곳이 아니에요.

<form id="suggest-form" class="suggest-form">
  <label for="suggest-artist">아티스트 이름</label>
  <input id="suggest-artist" name="artist" type="text" maxlength="200" placeholder="누구를 보면 좋을까요?" required>

  <label for="suggest-link">소셜 미디어 프로필 링크</label>
  <input id="suggest-link" name="link" type="url" maxlength="500" placeholder="https://www.instagram.com/…" required>

  <fieldset class="suggest-kinds">
    <legend>그분과 무엇을 하면 좋을까요?</legend>
    <label><input type="checkbox" name="kind" value="write"> 글 쓰기</label>
    <label><input type="checkbox" name="kind" value="interview"> 인터뷰하기</label>
    <label><input type="checkbox" name="kind" value="reaction"> 리액션 영상 만들기</label>
  </fieldset>

  <label for="suggest-why">왜 그분인가요?</label>
  <textarea id="suggest-why" name="why" rows="3" maxlength="500" placeholder="한두 마디면 충분해요…"></textarea>

  <label for="suggest-name">이름 <span class="optional">(선택 사항)</span></label>
  <input id="suggest-name" name="fromName" type="text" maxlength="100" placeholder="감사의 말을 전할 수 있게">

  <label for="suggest-from-link">내 소셜 미디어 프로필 링크 <span class="optional">(선택 사항)</span></label>
  <input id="suggest-from-link" name="fromLink" type="url" maxlength="500" placeholder="https://www.instagram.com/…">

  <button id="suggest-button" type="button">추천 보내기</button>

  <p id="suggest-result" aria-live="polite"></p>
</form>
