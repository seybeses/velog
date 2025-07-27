<h2 id="📝-문제-설명">📝 문제 설명</h2>
<p><img alt="" src="https://velog.velcdn.com/images/seybeses/post/c6d499b5-442b-4f00-bd71-d73740515bb7/image.png" /></p>
<h2 id="📥-입력--출력">📥 입력 &amp; 출력</h2>
<p><img alt="" src="https://velog.velcdn.com/images/seybeses/post/51a3bcda-0866-4d88-bb15-5ceb55d164a5/image.png" /></p>
<h2 id="💻-내-코드">💻 내 코드</h2>
<p>numlist에서 n으로 나누었을 때 나머지가 0이 되는 값을 answer 배열에 넣으면 된다고 생각했다. 그러려면 answer 배열의 크기를 알아내거나, ArrayList를 사용한다는 두 가지 선택지가 있었다. 아직 ArrayList 사용이 익숙하지 않기 때문에 배열 크기를 계산하는 방법을 선택했다.</p>
<pre><code class="language-java">class Solution {
    public int[] solution(int n, int[] numlist) {
        int count=0;
        for (int i=0; i&lt;numlist.length; i++){
                if(numlist[i]%n==0) count++;
        }

        int [] answer=new int[count];
        int index=0;
        for(int i=0; i&lt;numlist.length; i++){
            if (numlist[i]%n==0){
                answer[index]=numlist[i];
                index++;
            }      
        }
        return answer;
    }
}</code></pre>
<h3 id="💡-접근-방식">💡 접근 방식</h3>
<ol>
<li>answer 배열의 크기 구하기</li>
<li>answer 배열 생성</li>
<li>answer 배열에 값 삽입하기</li>
</ol>
<h2 id="✅-개선점">✅ 개선점</h2>
<h3 id="1-arraylist-사용">1. ArrayList 사용</h3>
<pre><code class="language-java">import java.util.ArrayList;

class Solution {
    public int[] solution(int n, int[] numlist) {
        ArrayList&lt;Integer&gt; list = new ArrayList&lt;&gt;();
        for (int num : numlist) {
            if (num % n == 0) {
                list.add(num);
            }
        }

        // ArrayList → int[] 배열로 변환
        int[] answer = new int[list.size()];
        for (int i = 0; i &lt; list.size(); i++) {
            answer[i] = list.get(i);
        }

        return answer;
    }
}
</code></pre>