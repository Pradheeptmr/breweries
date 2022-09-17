# breweries
program
document.body.innerHTML='
<div class="heading-container"
<h1> Brewerys list </h1>
<img> class="icon" src="https://image.shutterstock.com/image-vector/brewery-icon-design-concept-drinks-260nw-1205856094.jpg"></img>
</div>
<div id="mainContainer" Class="main-container"></div>

const getBreweriesData=asyn.()=>{
     try{
        const data=await fetch("https://api.openbrewerydb.org/breweries ");
        const Brewerys=await data.json();
        mainContainer.innerHtml="";
        brewerys.forEach((brewery))=>{
            displayBreweryData(brewery);
       }
      }catch(error){
        console.log(error);
      }
}
      getBreweriesData();


      const displayBreweryData=(obj)=>{
        mainContainer.innerHTML+=
        <div class="container">
              <h3 class="test">Name:<span>${obj.name}</span></h3>
              <p class="para test">Type:<span>${obj.brewery_type}</span></p>
              <p class="para test">Type:<span>${obj.city}</span></p>
              <p class="para test">Type:<span>${obj.state}</span></p>
              <p class="para test">Type:<span>${obj.street}</span></p>
              <p class="para test">Type:<span>${obj.phonetype}</span></p>
              <p class="para test">Type:<span>${obj.country}</span></p>


        </div>

      }
