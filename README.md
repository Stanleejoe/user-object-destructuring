# user-object-destructuring
const user = {  
    id: 123,  
    profile: {  
      name: "John Doe",  
      address: { city: "Los Angeles", zipcode: "90001" }  
    }  
  };  
  const { id, profile: { name, address: { city, zipcode } = { city: "Information not available", zipcode: "Information not available" } } = {} } = user;  
  const output = `${name} (ID: ${id}) lives in ${city || "Information not available"} with zipcode ${zipcode || "Information not available"}.`;  
console.log(output);
