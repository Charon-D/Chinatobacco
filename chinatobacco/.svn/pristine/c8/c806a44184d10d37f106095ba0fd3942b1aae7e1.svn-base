package com.chinatobacco.controller;

import java.util.List;

import org.apache.log4j.Logger;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.RequestMapping;

import com.chinatobacco.pojo.Repertory;
import com.chinatobacco.service.RepertoryService;

@Controller
@RequestMapping("/repertory")

public class RepertoryController {
	Logger logger = Logger.getLogger(RepertoryController.class);
	@Autowired
	private RepertoryService repertoryService;
	
	@RequestMapping("/list")
	public String list(Model model){
		List<Repertory> list=repertoryService.selectAll();
		model.addAttribute("list",list);
		return "showrepertory";
	}
	@RequestMapping("/toadd")
	public String toadd() {
		return "addrepertory";
	}

	@RequestMapping(value = "/add")
	public String add(Repertory repertory) {
		boolean flag = repertoryService.add(repertory);
		if (flag) {
			return "redirect:list.do";
		}
		return "404";
	}

	@RequestMapping("/delete")
	public String delete(int comid) {
		boolean flag = repertoryService.delete(comid);
		if (flag) {
			return "redirect:list.do";
		}
		return "404";
	}

	@RequestMapping("/toupdate")
	public String toupdate(String id,String comid,String num,String locid, Model model) {
		model.addAttribute("id", id);
		model.addAttribute("comid", comid);
		model.addAttribute("num", num);
		model.addAttribute("locid", locid);
		return "updaterepertory";
	}

	@RequestMapping("/update")
	public String update(Repertory repertory) {
		boolean flag = repertoryService.update(repertory);
		if (flag) {
			return "redirect:list.do";
		}
		return "404";
	}
}
