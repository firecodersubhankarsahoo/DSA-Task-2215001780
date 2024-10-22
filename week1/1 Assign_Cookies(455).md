```java


class Solution {
    public int findContentChildren(int[] g, int[] s) {
        Arrays.sort(g);
        Arrays.sort(s);
        int satisfied = 0;
        int i = s.length - 1;
        int j = g.length - 1;

        while (i >= 0 && j >= 0) {
            if (s[i] >= g[j]) {
                satisfied++;
                i--;
            }
            j--;
        }

        return satisfied;
    }
}

```