<h2 id="📦-주요-인터페이스">📦 주요 인터페이스</h2>
<table>
<thead>
<tr>
<th>인터페이스</th>
<th>설명</th>
<th>주요 구현체</th>
</tr>
</thead>
<tbody><tr>
<td><code>List</code> 📋</td>
<td>순서가 있는 데이터 저장, 중복 허용</td>
<td><code>ArrayList</code>, <code>LinkedList</code>, <code>Vector</code>, <code>Stack</code></td>
</tr>
<tr>
<td><code>Set</code> 🔑</td>
<td>중복 불가, 순서 없음(또는 정렬)</td>
<td><code>HashSet</code>, <code>LinkedHashSet</code>, <code>TreeSet</code></td>
</tr>
<tr>
<td><code>Map</code> 🗺️</td>
<td>키-값 쌍으로 저장</td>
<td><code>HashMap</code>, <code>LinkedHashMap</code>, <code>TreeMap</code>, <code>Hashtable</code></td>
</tr>
</tbody></table>
<hr />
<h2 id="📋-list-계열">📋 List 계열</h2>
<ul>
<li><strong>특징</strong>: 인덱스로 접근 가능, 중복 허용</li>
<li><strong>구현체 요약</strong></li>
</ul>
<table>
<thead>
<tr>
<th>클래스</th>
<th>특징</th>
</tr>
</thead>
<tbody><tr>
<td><code>ArrayList</code></td>
<td>배열 기반, 조회에 빠름</td>
</tr>
<tr>
<td><code>LinkedList</code></td>
<td>연결 리스트 기반, 삽입/삭제에 유리</td>
</tr>
<tr>
<td><code>Vector</code></td>
<td><code>ArrayList</code>와 유사하지만 <strong>동기화됨</strong></td>
</tr>
<tr>
<td><code>Stack</code></td>
<td>후입선출(LIFO), <code>Vector</code> 상속</td>
</tr>
</tbody></table>
<h3 id="✅-주요-메소드">✅ 주요 메소드</h3>
<table>
<thead>
<tr>
<th>메소드</th>
<th>설명</th>
</tr>
</thead>
<tbody><tr>
<td><code>add(E e)</code></td>
<td>요소 추가</td>
</tr>
<tr>
<td><code>add(int index, E element)</code></td>
<td>특정 위치에 요소 추가</td>
</tr>
<tr>
<td><code>get(int index)</code></td>
<td>인덱스로 요소 조회</td>
</tr>
<tr>
<td><code>set(int index, E element)</code></td>
<td>특정 인덱스의 값 수정</td>
</tr>
<tr>
<td><code>remove(int index)</code></td>
<td>특정 인덱스 요소 제거</td>
</tr>
<tr>
<td><code>indexOf(Object o)</code></td>
<td>특정 요소의 인덱스 반환</td>
</tr>
<tr>
<td><code>contains(Object o)</code></td>
<td>요소 존재 여부 확인</td>
</tr>
<tr>
<td><code>size()</code></td>
<td>요소 개수</td>
</tr>
<tr>
<td><code>clear()</code></td>
<td>모든 요소 제거</td>
</tr>
<tr>
<td><code>isEmpty()</code></td>
<td>비어 있는지 확인</td>
</tr>
<tr>
<td><code>iterator()</code></td>
<td>반복자 반환 (for-each용)</td>
</tr>
</tbody></table>
<hr />
<h2 id="🔑-set-계열">🔑 Set 계열</h2>
<ul>
<li><strong>특징</strong>: 중복 허용 ❌, 순서 없음(혹은 정렬됨)</li>
</ul>
<table>
<thead>
<tr>
<th>클래스</th>
<th>특징</th>
</tr>
</thead>
<tbody><tr>
<td><code>HashSet</code></td>
<td>가장 빠른 Set, 순서 없음</td>
</tr>
<tr>
<td><code>LinkedHashSet</code></td>
<td>입력 순서 유지</td>
</tr>
<tr>
<td><code>TreeSet</code></td>
<td>자동 정렬 (이진 트리 기반)</td>
</tr>
</tbody></table>
<h3 id="✅-주요-메소드-1">✅ 주요 메소드</h3>
<table>
<thead>
<tr>
<th>메소드</th>
<th>설명</th>
</tr>
</thead>
<tbody><tr>
<td><code>add(E e)</code></td>
<td>요소 추가</td>
</tr>
<tr>
<td><code>remove(Object o)</code></td>
<td>요소 제거</td>
</tr>
<tr>
<td><code>contains(Object o)</code></td>
<td>요소 존재 여부 확인</td>
</tr>
<tr>
<td><code>size()</code></td>
<td>요소 개수</td>
</tr>
<tr>
<td><code>clear()</code></td>
<td>모든 요소 제거</td>
</tr>
<tr>
<td><code>isEmpty()</code></td>
<td>비어 있는지 확인</td>
</tr>
<tr>
<td><code>iterator()</code></td>
<td>반복자 반환</td>
</tr>
<tr>
<td><code>addAll(Collection&lt;? extends E&gt; c)</code></td>
<td>여러 요소 한 번에 추가</td>
</tr>
</tbody></table>
<blockquote>
<p>❗ <code>Set</code>은 <code>get(int index)</code> 같은 인덱스 접근 메소드가 없음</p>
</blockquote>
<hr />
<h2 id="🗺️-map-계열">🗺️ Map 계열</h2>
<ul>
<li><strong>특징</strong>: 키는 중복 ❌, 값은 중복 ⭕  </li>
<li><strong>key로 빠르게 검색</strong> 가능</li>
</ul>
<table>
<thead>
<tr>
<th>클래스</th>
<th>특징</th>
</tr>
</thead>
<tbody><tr>
<td><code>HashMap</code></td>
<td>가장 일반적인 Map</td>
</tr>
<tr>
<td><code>LinkedHashMap</code></td>
<td>순서 유지</td>
</tr>
<tr>
<td><code>TreeMap</code></td>
<td>자동 정렬된 key 순서</td>
</tr>
<tr>
<td><code>Hashtable</code></td>
<td><code>HashMap</code>과 유사, <strong>동기화됨</strong></td>
</tr>
</tbody></table>
<h3 id="✅-주요-메소드-2">✅ 주요 메소드</h3>
<table>
<thead>
<tr>
<th>메소드</th>
<th>설명</th>
</tr>
</thead>
<tbody><tr>
<td><code>put(K key, V value)</code></td>
<td>키-값 추가 또는 수정</td>
</tr>
<tr>
<td><code>get(Object key)</code></td>
<td>키로 값 조회</td>
</tr>
<tr>
<td><code>remove(Object key)</code></td>
<td>키로 값 제거</td>
</tr>
<tr>
<td><code>containsKey(Object key)</code></td>
<td>키 존재 여부 확인</td>
</tr>
<tr>
<td><code>containsValue(Object value)</code></td>
<td>값 존재 여부 확인</td>
</tr>
<tr>
<td><code>size()</code></td>
<td>항목 개수</td>
</tr>
<tr>
<td><code>clear()</code></td>
<td>모든 항목 제거</td>
</tr>
<tr>
<td><code>isEmpty()</code></td>
<td>비어 있는지 확인</td>
</tr>
<tr>
<td><code>keySet()</code></td>
<td>모든 키 반환 (Set)</td>
</tr>
<tr>
<td><code>values()</code></td>
<td>모든 값 반환 (Collection)</td>
</tr>
<tr>
<td><code>entrySet()</code></td>
<td>키-값 쌍 (Map.Entry) 반환</td>
</tr>
</tbody></table>
<hr />
<h2 id="🔁-공통적으로-많이-쓰는-유틸리티-메소드">🔁 공통적으로 많이 쓰는 유틸리티 메소드</h2>
<table>
<thead>
<tr>
<th>메소드</th>
<th>설명</th>
</tr>
</thead>
<tbody><tr>
<td><code>Collections.sort(List&lt;T&gt;)</code></td>
<td>리스트 정렬</td>
</tr>
<tr>
<td><code>Collections.reverse(List&lt;T&gt;)</code></td>
<td>리스트 반전</td>
</tr>
<tr>
<td><code>Collections.shuffle(List&lt;T&gt;)</code></td>
<td>리스트 무작위 섞기</td>
</tr>
<tr>
<td><code>Collections.max(Collection&lt;T&gt;)</code></td>
<td>최대값 찾기</td>
</tr>
<tr>
<td><code>Collections.min(Collection&lt;T&gt;)</code></td>
<td>최소값 찾기</td>
</tr>
<tr>
<td><code>Collections.frequency(Collection&lt;T&gt;, Object o)</code></td>
<td>특정 요소 빈도</td>
</tr>
</tbody></table>
<hr />