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
