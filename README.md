# js-code
smaller than other arr

const smallNumber = (nums) =>{
	let copy  = [...nums];
  copy.sort();
  let hash = {};
  for(let i = 0; i < copy.length; i++){
  let num = copy[i];
  		if(hash[num] === undefined){
      		hash[num] = i; 
      }
  }
  return nums.map(num => hash[num]);
}

let nums = [8,4,1,2,2,3];
//console.log(nums.sort());

console.log(smallNumber(nums));

//VND format
const formatVND = (amount, prefix = '.') => {
  if (!amount) return null
  let a = amount.toString().replace(/\B(?=(\d{3})+(?!\d))/g, prefix)
  return a
}

//Sherlock and the Valid String
function isValid(s) {
  const cMap = {}
  for (let c of s) {
    cMap[c] ? cMap[c]++ : cMap[c] = 1
  }
  const freqs = new Set(Object.values(cMap))
  if (freqs.size === 1) return 'YES'
  if (freqs.size === 2) {
    const max = Math.max(...freqs)
    const min = Math.min(...freqs)
    let maxCt = 0
    let minCt = 0
    for (let c in cMap) {
      if (cMap[c] === max) maxCt++
      if (cMap[c] === min) minCt++
    }
    if (
      (minCt === 1 && min === 1) ||
      (maxCt === 1 && max === min + 1)
    ) return 'YES'
  }
  return 'NO'
}
////////////////////////////////////////////////////////////////////
const s = 'abcdefghhgfedecba'
isValid(s)
//=> YES
////////////////////////////////////////////////////////////////////
const s = 'aaaaabc'
isValid(s)
//=> NO

 Intl.NumberFormat

