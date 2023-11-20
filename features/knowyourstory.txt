import Footer from "@/components/Footer"
import styles from '../styles/Home.module.css'
import HomePageHeader from "@/components/HomePageHeader"
import { useState } from "react"

export default function KnowYourStory() {
  const [questions, setQuestions] = useState([])

    var randomNumber = Math.floor(Math.random() * 3)
    
  const fetchQuestions = async () => {
    const response = await fetch('/api/questions')
    const data = await response.json()
    
    var selectData = data.find(question => question.id == randomNumber)
    
    console.log(selectData)
    setQuestions(data)
  }      

  return (
    <>
      <div className={styles.container}>
          <HomePageHeader />
      <div className={styles.main}>
      <div className={styles.main_content}>
       <h1 className={styles.headline}>Know Your Story</h1>
       <h4 className={styles.headline_2}>A Random Q & A Generator to keep you on top of your game...</h4>
        <br />
       <br />
       <button onClick={fetchQuestions}>BUTTON HERE</button>

      </div>
        </div>
      <Footer />
      </div>
    </>
  )
}

