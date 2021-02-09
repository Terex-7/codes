# codes
function Filter(){
        let input=document.getElementById("the_input");
        let info=input.value.toUpperCase();
        let table=document.getElementById("List-of-marks");
        let row=table.getElementsByTagName("tr");
				for( i in row){
            for(let col=0;col<3;col++){
            		var data=row[i].getElementsByTagName("td")[col];
            		if(data){
                		let text=data.textContent || data.innerText;
                		if(text.toUpperCase().indexOf(info)>-1){
                   			 row[i].style.display=""; break;
               			 }
                		else{
                    			row[i].style.display="none";
                			}
            			}
        			}
					}
    }
