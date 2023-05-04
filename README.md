Download Link: https://assignmentchef.com/product/solved-csci-2500-assignment-6-openmp-prime-finder
<br>
Your task for this assignment is to implement a prime number finding program that utilizes multiple threads via OpenMP.

Prime numbers are useful in a variety of applications but probably most importantly in cryptography. For example, you may wish to look over the Wikipedia page for <a href="https://simple.wikipedia.org/wiki/RSA_(algorithm)">RSA</a><a href="https://simple.wikipedia.org/wiki/RSA_(algorithm)">.</a> Your program should return the number of unique primes that it was able to find within consecutive powers of ten.

As far as the method used for determining primes, there are <a href="https://en.wikipedia.org/wiki/Generating_primes">many possible approaches</a><a href="https://en.wikipedia.org/wiki/Generating_primes">.</a> One simple approach

<em>√</em>

is to try dividing your candidate <em>n </em>by values 2<em>,</em>3<em>,… n</em>. If the remainder is zero, then your <em>n </em>value is not prime. There are likely faster algorithms for producing prime values.

This may take a potentially long amount of time. The sizeable amounts of computation make this problem a good candidate for parallelizing via OpenMP. Fortunately, there is very little coordination required among the different threads. Your program should find all primes under 100,000,000.

The starter code will find the primes in a serial fashion but may not parallelize well. You may need to consider re-writing some of the logic to make the code more amenable for OpenMP. Also, you may need to mark some sections as critical.

Hopefully everyone can run their program on multiple cores.

Hopefully Submitty will allow us to use multiple cores as well &#x1f642;

<table width="195">

 <tbody>

  <tr>

   <td width="146">bash$ ./a.out</td>

   <td width="49"></td>

  </tr>

  <tr>

   <td width="146">10</td>

   <td width="49">4</td>

  </tr>

  <tr>

   <td width="146">100</td>

   <td width="49">25</td>

  </tr>

  <tr>

   <td width="146">1000</td>

   <td width="49">168</td>

  </tr>

  <tr>

   <td width="146">10000</td>

   <td width="49">1229</td>

  </tr>

  <tr>

   <td width="146">100000</td>

   <td width="49">9592</td>

  </tr>

  <tr>

   <td width="146">1000000</td>

   <td width="49">78498</td>

  </tr>

  <tr>

   <td width="146">10000000</td>

   <td width="49">664579</td>

  </tr>

  <tr>

   <td width="146">100000000</td>

   <td width="49">5761455</td>

  </tr>

 </tbody>

</table>

1