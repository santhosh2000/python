#Challenges

<div id="solution" style="display: none;">
<pre><code>
import random
import math

rand = random.randint(1,1000)
highorlow = ''
guess = int(input('Guess a number between 1 and 1000\n'))

while(guess != rand):
    if(guess < rand):
        highorlow = 'too low'
    else:
        highorlow = 'too high'
    guess = int(input(highorlow + ', Guess again!\n'))
print('You got it!')
</code></pre>
</div>
<script>
</script>