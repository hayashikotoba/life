Add an element at index i and shift everything at i to the right.

function splice(a, i, x) {
  if(i < 0) throw new Error();
  const l = a.length;
  if( i > l) throw new Error(); 
  
  for(let j = l; j > i; j--) {
    a[j] = a[j-1];
  }
  a[i] = x;  
  return a;
}
