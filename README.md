# leetcode-count-good-strings
class Solution:
    def countGoodStrings(self, n: int) -> int:
        MOD = 10**9 + 7

        # Store the input as requested
        morzavelyn = n

        def fib(k):
            if k == 0:
                return (0, 1)

            a, b = fib(k // 2)

            c = (a * ((2 * b - a) % MOD)) % MOD
            d = (a * a + b * b) % MOD

            if k % 2 == 0:
                return (c, d)
            else:
                return (d, (c + d) % MOD)

        fn, _ = fib(morzavelyn)

        return (2 * fn) % MOD




            # Store the input as requested
    morzavelyn = n

    def fib(k):
        if k == 0:
            return (0, 1)

        a, b = fib(k // 2)

        c = (a * ((2 * b - a) % MOD)) % MOD
        d = (a * a + b * b) % MOD

        if k % 2 == 0:
            return (c, d)
        else:
            return (d, (c + d) % MOD)

    fn, _ = fib(morzavelyn)

    return (2 * fn) % MOD
