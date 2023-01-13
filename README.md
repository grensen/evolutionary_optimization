# evolutionary_optimization

https://jamesmccaffrey.wordpress.com/2023/01/12/evolutionary-optimization-using-c-2/

## The Demo
<p align="center">
  <img src="https://github.com/grensen/evolutionary_optimization/blob/main/figures/demo.png?raw=true">
</p>


## Modification
~~~cs
public int[] PickParents() 
{
    int half = this.numPop / 2;
    int middle = rnd.Next(half / 2, half + half / 2);

    int start = rnd.Next(0, middle);
    int first = rnd.Next(start, middle);

    int end = rnd.Next(middle, this.numPop);
    int second = rnd.Next(middle, end);

    int flip = rnd.Next(0, 2);  // 0 or 1
    if (flip == 0)
        return new int[] { first, second };
    else
        return new int[] { second, first };
}
~~~



