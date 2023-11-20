import Footer from "@/components/Footer"
import styles from '../styles/Home.module.css'
import Header from "@/components/HomePageHeader"
// import styles from '../styles/FutureFeature.module.css'

export default function Home() {
  return (
    <>
     
     <div className={styles.container}>
          <Header />
      <div className={styles.main}>
      <div className={styles.main_content}>

       <h1 className={styles.headline}>Send Download Link to Customer</h1>

          <br />
            <div className={styles.form}>
                <label for="name">Customer Id Number:</label>
                <input type="text" id="name" name="name" placeholder="Customer ID Number"/>
                
                <label for="email">Customer Cell Phone Number:</label>
                <input type="email" id="email" name="email" placeholder="Customer Cell Phone"/>
                
                <input type="submit" value="Submit"/>
            </div>
          <div>
            
          </div>

      </div>
      </div>
      
         
        </div>


      <Footer />

    </>
  )
}
