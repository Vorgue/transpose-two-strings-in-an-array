# transpose-two-strings-in-an-array

function transposeTwoStrings(arr){
	var max_length = Math.max(...arr.map(x => x.length));
	var str = '';
	for (var i = 0; i < max_length; i++) {
		for (var j = 0; j < arr.length; j++) {
			if (arr[j].length - 1 >= i) {str = str + arr[j].charAt(i)}
			else {str = str + ' '};
			if (j < arr.length - 1) {str = str + ' '}
		}
	if (i < max_length - 1) {str = str + "\n"}
	}
	return str
}
