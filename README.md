


import './Product.css'
import Price from './Price.jsx';
function Product({title,idx,des}) {
   

   
   let oldprices=["12,995","11,900","1,599","999"];
   let newprices=["8,999","9,199","800","270"];
   let styles={
      height:"220px",
      width:"500px",
      border:"2px solid black",
      color:"black",
      borderRadius:"10px",
      marginTop:"20px",
      marginRight:"20px"
   }
    return (
              <div style={styles}>
              <h3>{title}</h3>
              <p>{des[idx][0]}</p>
              <p>{des[idx][1]}</p>
            <Price oldPrice={oldprices[idx]} newPrice={newprices[idx]}/>
              </div>
          
    )

}
export default Product


import Product from './Product.jsx';
function ProductTab(){
    let description=[["good surface","nice touch"],["touchpad","ipad pro max"],["nano chip technology","radium beam"],["incomper","high definition"]];
    let styles={
        display:"flex",
        flex:"wrap",
        justifyContent:"center",
        alignItems:"center"
    }
    return (
        <div style={styles} >
            <Product title="Logitech MX Master" idx={0} des={description}/>
            <Product title="Apple Pencil(2nd Gen)" idx={1} des={description}/>
            <Product title="Zebronics Zeb-Transformer" idx={2} des={description}/>
            <Product title="Wireless 3D Mouse" idx={3} des={description}/>
        </div>
    )
}
export default ProductTab

function Price({oldPrice,newPrice}){
    let styles={
        width: "299px",
        height: "60px",
        backgroundColor: "yellow",
        borderRadius: "0px 0px 7px 10px",
        marginTop: "31px",
       
        
       
    }
    let oldstyle={
        backgroundColor: "yellow",
        alignItems:"center",
        textDecorationLine:"line-through",

    }
    let newstyle={
        fontWeight:"bold",
        backgroundColor: "yellow"
    }
   
       

    
    return (
        <div className="par"style={styles}>
          <span style={  oldstyle
          }>{oldPrice}</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          <span style={newstyle}>{newPrice}</span>
        </div>
    )
}
export default Price


import './App.css'
import ProductTab from './ProductTab.jsx';
function App(){
  
  return (
    <div>
<ProductTab/>

    </div>
   
  )
}
export default App


