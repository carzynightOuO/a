function bsearch(a, o, from, to) {
    if (from > to) return null
    var mid = Math.floor((from + to)/2)
    if (a[mid] === o)
       return mid
    if (o > a[mid])
       return bsearch(a, o, mid+1, to)
    else // o < a[mid]
       return bsearch(a, o, 0, mid-1)
  }
  
  function search(a, o) {
     var n = a.length
     return bsearch(a, o, 0, n)
  }
  for(var c=1; c<=10; c++)
  {
   var t = search([1, 3, 4, 6, 7, 8],c)
   console.log(`ans=${t}`)
   }
    
