

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class DestroyScript : MonoBehaviour
{
    //someone people tried to help me with this script
    public GameObject GameManager;
    
    // Start is called before the first frame update
   

     private void OnCollisionEnter2D(Collision2D collision)
    {
                  
        if(collision.gameObject.tag == "Ball")
       {
            Destroy(collision.gameObject);
       }
    }  
      
}


using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class ScoreScript : MonoBehaviour
{
          public int Score;
    public void OnCollisionEnter2D(Collision2D collision)
    {
  

        //Students helped me with this one 
        if(collision.gameObject.tag == "Bumper")
        {
            Score += 100;
        }
    }
}

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PaddleScript : MonoBehaviour
{
    
        public Vector3 rotateleft;
     public Vector3 rotateright;

    // Update is called once per frame
    void Update()
    {
              if (Input.GetKey(KeyCode.A))
      {
        GetComponent<Transform>() .position += rotateleft;
      }
      if (Input.GetKey(KeyCode.D))
      {
        GetComponent<Transform>() .position += rotateright;
      }
    }
}

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using TMPro;

public class LeaderBoardScript : MonoBehaviour
{
    private List<string> playerNames = new List<string>{"Miguel", "Greyson", "Jayleen", "Max", "Kyle"};
    private List<int> playerScores = new List<int>{ 100, 200, 300, 400, 500 };

    void Start()
    {
     
    }

    // Update is called once per frame
    void Update()
    {

    }
    
void UpdateLeaderBoard()
    {
     for (int i = 0;  playerScores.Count; i++);{}
    }
}
