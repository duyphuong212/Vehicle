# THB1
package bt1a.newpackage;

/**
 *
 * @author MSI-PC
 */
public class Vehicle {
   
	   private int maXe, dungTich;
	   private double triGia;
	   private String chuXe;

	public Vehicle(int maXe, int dungTich, double triGia, String chuXe){
	    this.maXe = maXe;
	    this.dungTich = dungTich;
	    this.triGia = triGia;
	    this.chuXe = chuXe;
	}
	public Vehicle(){

	}
	  public int getMaXe(){
	    return maXe;
	}
	  public void setMaXe( int maXe){
	    this.maXe = maXe;
	  }
	  public int getDungTich(){
	     return dungTich;
	}
	public void setDungTich(int dungTich){
	    this.dungTich = dungTich;
	}
	public double getTriGia(){
	    return triGia;
	}
	public void setTriGia(double triGia){
	    this.triGia = triGia;
	}
	public String getChuXe(){
	    return chuXe;
	}
	public void setChuXe(String chuXe){
	    this.chuXe = chuXe;
	}
	  public double tinhThue(){
	   double thue;
	   if(dungTich<100) thue = triGia*0.01;
	   else if (dungTich >= 100 && dungTich <=200) thue = triGia*0.03;
	   else thue = triGia * 0.05;
	   return thue;
	}
	@Override
	public String toString(){
	    return maXe + "-"+chuXe + "-"+dungTich+"-"+triGia;
	}
	void inThue(){
	    System.out.printf("%5d %-20s %5d %10.2f %8.5f \n", maXe,chuXe,dungTich,triGia,tinhThue());
	}
	}
