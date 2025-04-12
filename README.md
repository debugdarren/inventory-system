items=({});
function viewItems(){
  if(items === ""){
    var Nan = prompt("Nothing here please add items.\n" +"Press z to go back")
    if(Nan == z){
      main();
    }else{
      alert("Error:not in prompt:(");
    };
  } else {
    alert("all items are here:\n" + items[0][name] + "RM" + items[0][price] + items[0][quantity]);
    }
  }
  main();


function addItem(){
  var name = prompt("Name the item you want to add");
  var price = prompt("What is the price of " + name);
  var quantity = prompt("How many/much you want of " + name);
  alert("sucessfully added " + name)
  items.push({
    name: name,
    price: price,
    quantity: quantity
  });
  main();
}

function main(){
  var input = prompt("Debug Lab Inventory System\nPress 0 to view all items\nPress z to close\nPress 1 to add item");

  if(input == "0"){
    viewItems();
  }
  else if(input == "z"){
    return 0;
  } else if(input == "1"){
    addItem();
  } else {
    alert("Error:not in prompt:(");
    main();
  }
}
main();
