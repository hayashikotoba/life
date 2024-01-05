Prompt: Remove Duplicates from sorted array 


Q: do you want in place or copy?

// This assumes the array is sorted.
function removeDupes(a) {
  const b = [];

  let i = 0;
  while(i < a.length) {
    let x = a[i];
    b.push(x);
    while(i < a.length && a[i] == x) {
      i++;
    }
  }
  
  return b;
}

// This doesn't care if array is sorted
function removeDupes(a) {
  const s = new Set();
  for(let i = 0; i < a.length; i++)
    s.add(a[i]);

  return Array.from(s.keys());
}
