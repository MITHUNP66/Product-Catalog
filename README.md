# Product-Catalog
This Java program demonstrates the use of inheritance and method overriding through a simple product catalog system. A base class Product is extended by two subclasses: Ele for electronic items and Clot for clothing. Each subclass adds its own attributes and overrides the display() method to show detailed product information.

code:
package com.recuse;
class product {
	String name="mit";
	double price=1000;
	
	product(String name,double price){
	this.name=name;
	this.price=price;
}
	public void display() {
		System.out.println("name :"+name);
		System.out.println("price :"+ price);
	}
}
	class ele extends product{
		String brand;
		int warr;
		
		ele(String name,double price,String brand,int warr){
			super(name,price);
			this.brand=brand;
			this.warr=warr;
			
		}	
		
		//@Override
		public void display() {
			super.display();
			
			System.out.println("brand :"+brand);
			System.out.println("warr :"+warr );
			}
	}

		class clot extends product{
			String size;
			String mat;
			clot(String name,double price,String size,String mat){
				super(name,price);
				this.size=size;
				this.mat=mat;
				
			}
			
			public void display() {
				super.display();
				System.out.println("size :"+size);
				System.out.println("mat :"+mat );
				}
	}
		
	
public class classtes {

	public static void main(String[] args) {
		
          ele e=new ele("mitun",30000,"tui",3);
          e.display();
           System.out.println();
           clot c=new clot("mitun",30,"m","cotton");
          c.display();
 	}
 }

